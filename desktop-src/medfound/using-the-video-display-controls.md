---
description: Usando os controles de exibição de vídeo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Usando os controles de exibição de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647731"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="99164-103">Usando os controles de exibição de vídeo</span><span class="sxs-lookup"><span data-stu-id="99164-103">Using the Video Display Controls</span></span>

<span data-ttu-id="99164-104">A interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) controla como o processador de vídeo avançado (EVR) exibe vídeo dentro de uma janela de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99164-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="99164-105">Essa interface pode ser usada tanto no DirectShow quanto no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="99164-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="99164-106">Internamente, os controles de exibição de vídeo são fornecidos pelo apresentador padrão da EVR.</span><span class="sxs-lookup"><span data-stu-id="99164-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="99164-107">Se você escrever um apresentador personalizado, poderá fornecer a mesma interface ou definir uma interface personalizada.</span><span class="sxs-lookup"><span data-stu-id="99164-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="99164-108">A maneira correta de obter um ponteiro para a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) depende se você está usando a versão do DIRECTSHOW do EVR ou a versão Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="99164-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="99164-109">Para o Media Foundation EVR, também depende se você está usando o EVR diretamente ou usando-o por meio da sessão de mídia (que é mais comum).</span><span class="sxs-lookup"><span data-stu-id="99164-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="99164-110">Para obter um ponteiro para a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="99164-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="99164-111">Obtenha um ponteiro para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="99164-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="99164-112">Se você estiver usando o filtro EVR do DirectShow, chame **QueryInterface** no filtro.</span><span class="sxs-lookup"><span data-stu-id="99164-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="99164-113">Se você estiver usando o coletor de mídia do EVR diretamente, chame **QueryInterface** no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="99164-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="99164-114">Se você estiver usando a sessão de mídia, chame **QueryInterface** na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="99164-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="99164-115">Se você estiver usando a sessão de mídia, aguarde até que a sessão de mídia envie o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com um valor de status de MF \_ TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="99164-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="99164-116">(Ignore esta etapa de outra forma.)</span><span class="sxs-lookup"><span data-stu-id="99164-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="99164-117">Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="99164-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="99164-118">O identificador de serviço é o \_ serviço de renderização de vídeo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="99164-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="99164-119">Você pode usar a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="99164-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="99164-120">Defina a janela de recorte.</span><span class="sxs-lookup"><span data-stu-id="99164-120">Set the clipping window.</span></span>

-   <span data-ttu-id="99164-121">Defina os retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="99164-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="99164-122">Atualize a janela de vídeo em resposta a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="99164-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="99164-123">Habilitar ou desabilitar o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="99164-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="99164-124">Janela de recorte</span><span class="sxs-lookup"><span data-stu-id="99164-124">Clipping Window</span></span>

<span data-ttu-id="99164-125">O aplicativo deve fornecer uma janela onde o EVR desenha o vídeo.</span><span class="sxs-lookup"><span data-stu-id="99164-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="99164-126">Para definir a janela de recorte, chame [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) com um identificador para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99164-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="99164-127">Se você criar o coletor de mídia do EVR por meio de seu objeto de ativação, essa etapa não será necessária.</span><span class="sxs-lookup"><span data-stu-id="99164-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="99164-128">O objeto de ativação chama automaticamente [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), usando o identificador de janela que você forneceu na função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="99164-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="99164-129">Retângulos de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="99164-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="99164-130">Durante a reprodução, o apresentador usa uma parte da imagem de vídeo compostada e a desenha em uma área da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="99164-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="99164-131">A parte da imagem composta é o retângulo de *origem* e a área da janela de vídeo é o retângulo de *destino*.</span><span class="sxs-lookup"><span data-stu-id="99164-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="99164-132">O retângulo de origem é definido usando coordenadas normalizadas em que o ponto (0,0, 0,0) corresponde ao canto superior esquerdo do vídeo e (1,0, 1,0) corresponde ao canto inferior direito do vídeo.</span><span class="sxs-lookup"><span data-stu-id="99164-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="99164-133">O retângulo de origem pode ser qualquer região dentro deste retângulo.</span><span class="sxs-lookup"><span data-stu-id="99164-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="99164-134">O retângulo de destino é especificado em pixels, em relação à área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="99164-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="99164-135">O retângulo de origem padrão é a imagem inteira e o retângulo de destino padrão é um retângulo vazio.</span><span class="sxs-lookup"><span data-stu-id="99164-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="99164-136">Para definir os retângulos de origem e de destino, chame [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="99164-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="99164-137">Se você criar o coletor de mídia do EVR por meio de seu objeto de ativação, essa etapa não será necessária.</span><span class="sxs-lookup"><span data-stu-id="99164-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="99164-138">O objeto de ativação define automaticamente o retângulo de destino igual a toda a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="99164-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="99164-139">No entanto, você deve chamar [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) se quiser alterar o retângulo de origem ou definir um retângulo de destino diferente.</span><span class="sxs-lookup"><span data-stu-id="99164-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="99164-140">Mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="99164-140">Window Messages</span></span>

<span data-ttu-id="99164-141">Durante a reprodução, o aplicativo deve responder a determinadas mensagens da janela, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="99164-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="99164-142">WM \_ Paint: chame [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) para redesenhar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="99164-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="99164-143">Além disso, evite pintar o retângulo de destino enquanto o vídeo está sendo reproduzido, pois isso pode causar oscilação.</span><span class="sxs-lookup"><span data-stu-id="99164-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="99164-144">\_Tamanho do WM: Talvez seja necessário chamar [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) para redimensionar o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="99164-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="99164-145">Diferentemente do filtro de processador de mixagem de vídeo (VMR) no DirectShow, você não precisa notificar o EVR ao receber uma mensagem do WM \_ DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="99164-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99164-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99164-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99164-147">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="99164-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



