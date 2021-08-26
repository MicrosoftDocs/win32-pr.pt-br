---
title: Exemplo de código de formato de pixel GLX
description: O exemplo de código a seguir mostra como um programa OpenGL do sistema de janelas X usa funções de formatação visual/pixel GLX.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- portando para OpenGL, pixels
- Portabilidade do OpenGL, pixels
- X sistema de janelas, pixels
- Funções GLX, pixels
- pixels, exemplo de GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312b95fb2ff4719c9ecda863b67ac926905b09d0e4b8aecbcc673a03c18c307a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035377"
---
# <a name="glx-pixel-format-code-sample"></a>Exemplo de código de formato de pixel GLX

O exemplo de código a seguir mostra como um programa OpenGL do sistema de janelas X usa funções de formatação visual/pixel GLX.


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



O Visual pode ser usado para criar uma janela e um contexto de renderização.

 

 




