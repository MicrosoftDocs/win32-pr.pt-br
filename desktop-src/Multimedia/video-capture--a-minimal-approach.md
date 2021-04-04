---
title: Captura de vídeo de uma abordagem mínima
description: Captura de vídeo de uma abordagem mínima
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Vídeo para Windows (VFW), captura de vídeo
- VFW (vídeo para Windows), captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823707"
---
# <a name="video-capture-a-minimal-approach"></a><span data-ttu-id="43c98-105">Captura de vídeo: uma abordagem mínima</span><span class="sxs-lookup"><span data-stu-id="43c98-105">Video Capture: A Minimal Approach</span></span>

<span data-ttu-id="43c98-106">A captura de vídeo digitaliza um fluxo de dados de áudio e vídeo e o armazena em um disco rígido ou algum outro tipo de dispositivo de armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="43c98-106">Video capture digitizes a stream of video and audio data, and stores it on a hard disk or some other type of persistent storage device.</span></span> <span data-ttu-id="43c98-107">Esta seção descreve como adicionar uma forma simples de captura de vídeo a um aplicativo usando três instruções de código.</span><span class="sxs-lookup"><span data-stu-id="43c98-107">This section describes how to add a simple form of video capture to an application using three statements of code.</span></span> <span data-ttu-id="43c98-108">Ele também descreve como terminar ou abortar uma sessão de captura enviando mensagens para a janela de captura.</span><span class="sxs-lookup"><span data-stu-id="43c98-108">It also describes how to end or abort a capture session by sending messages to the capture window.</span></span>

<span data-ttu-id="43c98-109">Uma janela de captura AVICap lida com os detalhes do streaming de áudio e captura de vídeo para arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="43c98-109">An AVICap capture window handles the details of streaming audio and video capture to AVI files.</span></span> <span data-ttu-id="43c98-110">Isso libera seu aplicativo do envolvimento no formato de arquivo AVI, no gerenciamento do buffer de vídeo e de áudio e no acesso de baixo nível de drivers de dispositivo de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="43c98-110">This frees your application from involvement in the AVI file format, video and audio buffer management, and the low-level access of video and audio device drivers.</span></span> <span data-ttu-id="43c98-111">O AVICap fornece uma interface flexível para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="43c98-111">AVICap provides a flexible interface for applications.</span></span> <span data-ttu-id="43c98-112">Você pode adicionar a captura de vídeo ao seu aplicativo usando apenas as seguintes linhas de código:</span><span class="sxs-lookup"><span data-stu-id="43c98-112">You can add video capture to your application, using only the following lines of code:</span></span>


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



<span data-ttu-id="43c98-113">Também está disponível uma interface de macro que fornece uma alternativa ao uso da função [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) e melhora a legibilidade de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43c98-113">A macro interface is also available that provides an alternative to using the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function and improves the readability of an application.</span></span> <span data-ttu-id="43c98-114">O exemplo a seguir usa a interface de macro para adicionar captura de vídeo a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43c98-114">The following example uses the macro interface to add video capture to an application.</span></span>


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



<span data-ttu-id="43c98-115">Depois que o aplicativo cria uma janela de captura da classe de janela AVICap e a conecta a um driver de vídeo, a janela de captura está pronta para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="43c98-115">After your application creates a capture window of the AVICap window class and connects it to a video driver, the capture window is ready to capture data.</span></span> <span data-ttu-id="43c98-116">Neste ponto, o aplicativo pode simplesmente enviar a mensagem [**de \_ \_ sequência do WM Cap**](wm-cap-sequence.md) (ou a macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) para começar a capturar.</span><span class="sxs-lookup"><span data-stu-id="43c98-116">At this point, your application can simply send the [**WM\_CAP\_SEQUENCE**](wm-cap-sequence.md) message (or the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro) to begin capturing.</span></span>

<span data-ttu-id="43c98-117">Usando as configurações padrão, \_ a \_ sequência de extremidade do WM inicia a captura de vídeo e entrada de áudio para um arquivo chamado CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="43c98-117">Using default settings, WM\_CAP\_SEQUENCE initiates the capture of video and audio input to a file named CAPTURE.AVI.</span></span> <span data-ttu-id="43c98-118">A captura continua até que ocorra um dos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="43c98-118">Capture continues until one of the following events occurs:</span></span>

-   <span data-ttu-id="43c98-119">O usuário pressiona a tecla ESC ou um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="43c98-119">The user presses the ESC key or a mouse button.</span></span>
-   <span data-ttu-id="43c98-120">O aplicativo para de ou anula a operação de captura.</span><span class="sxs-lookup"><span data-stu-id="43c98-120">Your application stops or aborts capture operation.</span></span>
-   <span data-ttu-id="43c98-121">O disco fica cheio.</span><span class="sxs-lookup"><span data-stu-id="43c98-121">The disk becomes full.</span></span>

<span data-ttu-id="43c98-122">Em um aplicativo, você pode parar o streaming de dados capturados em um arquivo enviando a mensagem do [**WM \_ Cap \_ Stop**](wm-cap-stop.md) (ou a macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="43c98-122">In an application, you can stop streaming captured data to a file by sending the [**WM\_CAP\_STOP**](wm-cap-stop.md) (or the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro) message to a capture window.</span></span> <span data-ttu-id="43c98-123">Você também pode anular a operação de captura enviando a mensagem de [**\_ \_ anulação do WM Cap**](wm-cap-abort.md) (ou a macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="43c98-123">You can also abort the capture operation by sending the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message (or the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro) to a capture window.</span></span>

 

 