---
title: Criando um contexto de renderização e tornando-o atual
description: O exemplo de código a seguir mostra como criar um contexto de renderização OpenGL em resposta a uma mensagem de criação do WM \_ .
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL no Windows, contextos de renderização
- contextos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292480"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Criando um contexto de renderização e tornando-o atual

O exemplo de código a seguir mostra como criar um contexto de renderização OpenGL em resposta a uma mensagem de criação do WM \_ . Observe que você configurou o formato de pixel antes de criar o contexto de renderização. Observe também que, nesse cenário, o contexto do dispositivo não é liberado localmente; Você o libera quando a janela é fechada, depois de tornar o contexto de renderização não atual. Para obter mais informações, consulte [excluindo um contexto de renderização](deleting-a-rendering-context.md). Por fim, observe que você pode usar variáveis locais para o contexto do dispositivo e processar identificadores de contexto, porque com as funções [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) e [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) , você pode obter identificadores para esses contextos conforme necessário.

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

 

 




