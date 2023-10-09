---
title: "How to render a diagram, using kroki plugin"
date: 2023-11-07
draft: false 
authors:
  - myspotontheweb
categories:
  - Diagrams
---

Kroki is a hosted service creating diagrams from textual descriptions

* [https://kroki.io/](https://kroki.io)

This demonstrates how it can be integrated with MkDocs

<!-- more -->

## blockdiag

```kroki-blockdiag no-transparency=false
blockdiag {
  blockdiag -> generates -> "block-diagrams";
  blockdiag -> is -> "very easy!";

  blockdiag [color = "greenyellow"];
  "block-diagrams" [color = "pink"];
  "very easy!" [color = "orange"];
}
```

## Structurizr

```kroki-Structurizr
 workspace {
    model { 
        user = person "User" 
        softwareSystem = softwareSystem "Software System" { 
            webapp = container "Web Application" { 
                user -> this "Uses!!!" 
            } 
            database = container "Database" { 
                webapp -> this "Reads from and writes to" 
            } 
        } 
    } 
    views { 
        systemContext softwareSystem { 
            include * 
            autolayout lr 
        } 
        container softwareSystem { 
            include * 
            autolayout lr 
        } 
        theme default 
    } 
}
```

## seqdiag

```kroki-seqdiag
seqdiag {
  browser  -> webserver [label = "GET /seqdiag/svg/base64"];
  webserver  -> processor [label = "Convert text to image"];
  webserver <-- processor;
  browser <-- webserver;
}
```
