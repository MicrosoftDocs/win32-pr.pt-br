---
title: Excluindo um contexto de renderização
description: O exemplo de código a seguir mostra como excluir um contexto de renderização OpenGL quando uma janela OpenGL é fechada. É uma continuação do cenário usado em Criando um contexto de renderização e tornando-o atual.
ms.assetid: 562c4698-f5bb-418a-8479-0df07e9834e5
keywords:
- OpenGL em Windows, renderização de contextos
- contextos de renderização OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6821e51ad2493bc2ec3ce1c3ce9b448faee1079ae3771cf3290874fcb9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889236"
---
# <a name="deleting-a-rendering-context"></a>Excluindo um contexto de renderização

O exemplo de código a seguir mostra como excluir um contexto de renderização OpenGL quando uma janela OpenGL é fechada. É uma continuação do cenário usado em Criando um contexto de renderização [e tornando-o atual.](creating-a-rendering-context-and-making-it-current.md)


```C++
// a window is about to be destroyed  
case WM_DESTROY: 
    { 
    // local variables  
    HGLRC    hglrc; 
    HDC      hdc ; 
 
    // if the thread has a current rendering context ...  
    if(hglrc = wglGetCurrentContext()) { 
 
        // obtain its associated device context  
        hdc = wglGetCurrentDC() ; 
 
        // make the rendering context not current  
        wglMakeCurrent(NULL, NULL) ; 
 
        // release the device context  
        ReleaseDC (hwnd, hdc) ; 
 
        // delete the rendering context  
        wglDeleteContext(hglrc); 
 
        }
```



 

 




