---
title: Criando um contexto de renderização e tornando-o atual
description: O exemplo de código a seguir mostra como criar um contexto de renderização OpenGL em resposta a uma mensagem WM \_ CREATE.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL em Windows, renderização de contextos
- contextos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1768506eba506506a7198fbccc7dfefc0491adc96dd1e7bd03d2ec2aa5df8eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868786"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Criando um contexto de renderização e tornando-o atual

O exemplo de código a seguir mostra como criar um contexto de renderização OpenGL em resposta a uma mensagem WM \_ CREATE. Observe que você configura o formato de pixel antes de criar o contexto de renderização. Observe também que, nesse cenário, o contexto do dispositivo não é liberado localmente; você a libera quando a janela é fechada, depois de tornar o contexto de renderização não atual. Para obter mais informações, consulte [Excluindo um contexto de renderização](deleting-a-rendering-context.md). Por fim, observe que você pode usar variáveis locais para o contexto do dispositivo e os alças de contexto de renderização, porque com as funções [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) e [**wglGetCurrentDC,**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) você pode obter os handles para esses contextos conforme necessário.

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




