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
# <a name="creating-a-rendering-context-and-making-it-current"></a><span data-ttu-id="22634-105">Criando um contexto de renderização e tornando-o atual</span><span class="sxs-lookup"><span data-stu-id="22634-105">Creating a Rendering Context and Making It Current</span></span>

<span data-ttu-id="22634-106">O exemplo de código a seguir mostra como criar um contexto de renderização OpenGL em resposta a uma mensagem de criação do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="22634-106">The following code sample shows how to create an OpenGL rendering context in response to a WM\_CREATE message.</span></span> <span data-ttu-id="22634-107">Observe que você configurou o formato de pixel antes de criar o contexto de renderização.</span><span class="sxs-lookup"><span data-stu-id="22634-107">Notice that you set up the pixel format before creating the rendering context.</span></span> <span data-ttu-id="22634-108">Observe também que, nesse cenário, o contexto do dispositivo não é liberado localmente; Você o libera quando a janela é fechada, depois de tornar o contexto de renderização não atual.</span><span class="sxs-lookup"><span data-stu-id="22634-108">Also notice that in this scenario the device context is not released locally; you release it when the window is closed, after making the rendering context not current.</span></span> <span data-ttu-id="22634-109">Para obter mais informações, consulte [excluindo um contexto de renderização](deleting-a-rendering-context.md).</span><span class="sxs-lookup"><span data-stu-id="22634-109">For more information, see [Deleting a Rendering Context](deleting-a-rendering-context.md).</span></span> <span data-ttu-id="22634-110">Por fim, observe que você pode usar variáveis locais para o contexto do dispositivo e processar identificadores de contexto, porque com as funções [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) e [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) , você pode obter identificadores para esses contextos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="22634-110">Finally, notice that you can use local variables for the device context and rendering context handles, because with the [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) and [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) functions you can obtain handles to those contexts as needed.</span></span>

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

 

 




