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
ms.openlocfilehash: 9f0ab6464d54e696c136a6c987b94124f52b0ee2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635007"
---
# <a name="glx-pixel-format-code-sample"></a><span data-ttu-id="605db-108">Exemplo de código de formato de pixel GLX</span><span class="sxs-lookup"><span data-stu-id="605db-108">GLX Pixel Format Code Sample</span></span>

<span data-ttu-id="605db-109">O exemplo de código a seguir mostra como um programa OpenGL do sistema de janelas X usa funções de formatação visual/pixel GLX.</span><span class="sxs-lookup"><span data-stu-id="605db-109">The code sample below shows how an X Window System OpenGL program uses GLX visual/pixel formatting functions.</span></span>


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



<span data-ttu-id="605db-110">O Visual pode ser usado para criar uma janela e um contexto de renderização.</span><span class="sxs-lookup"><span data-stu-id="605db-110">The Visual can be used to create a window and a rendering context.</span></span>

 

 




