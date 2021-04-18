---
title: Adicionando funções de retorno de chamada a um aplicativo
description: Adicionando funções de retorno de chamada a um aplicativo
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498712"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="03632-103">Adicionando funções de retorno de chamada a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="03632-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="03632-104">Um aplicativo pode registrar funções de retorno de chamada com a janela de captura para que ela notifique o aplicativo nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="03632-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="03632-105">O status é alterado</span><span class="sxs-lookup"><span data-stu-id="03632-105">The status changes</span></span>
-   <span data-ttu-id="03632-106">Ocorreram erros</span><span class="sxs-lookup"><span data-stu-id="03632-106">Errors occur</span></span>
-   <span data-ttu-id="03632-107">Quadros de vídeo e buffers de áudio tornam-se disponíveis</span><span class="sxs-lookup"><span data-stu-id="03632-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="03632-108">O aplicativo deve produzir durante a captura de streaming</span><span class="sxs-lookup"><span data-stu-id="03632-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="03632-109">O exemplo a seguir cria uma janela de captura e registra as funções de status, erro, fluxo de vídeo e retorno de chamada de quadro no loop de processamento de mensagens de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="03632-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="03632-110">Ele também inclui uma instrução de exemplo para desabilitar uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="03632-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="03632-111">Os exemplos subsequentes mostram as funções de retorno de chamada de status, erro e quadro simples.</span><span class="sxs-lookup"><span data-stu-id="03632-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="03632-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03632-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03632-113">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="03632-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




