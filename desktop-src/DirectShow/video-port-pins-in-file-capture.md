---
description: Pins de porta de vídeo na captura de arquivo
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Pins de porta de vídeo na captura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775590"
---
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="e2f98-103">Pins de porta de vídeo na captura de arquivo</span><span class="sxs-lookup"><span data-stu-id="e2f98-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="e2f98-104">Se o dispositivo de captura tiver uma porta de vídeo, o PIN da porta de vídeo deverá ser conectado a um processador de vídeo, mesmo que você queira apenas capturar para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2f98-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="e2f98-105">Se você chamar [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com o valor **fixar \_ categoria \_ Capture** e o dispositivo tiver um pino de porta de vídeo, o construtor do grafo de captura conectará automaticamente o PIN da porta de vídeo ao filtro do [mixer de sobreposição](overlay-mixer-filter.md) e conectará o mixer de sobreposição ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2f98-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="e2f98-106">O construtor do grafo de captura oculta a janela de vídeo chamando [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) com o valor **OAFALSE**.</span><span class="sxs-lookup"><span data-stu-id="e2f98-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="e2f98-107">Se o aplicativo mais tarde chamar **RenderStream** com a **\_ \_ visualização de categoria de PIN**, as chamadas do construtor de grafo de captura **colocarão \_ AutoShow** com o valor **OATRUE** para mostrar a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2f98-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="e2f98-108">Depois de chamar **RenderStream** com **a \_ \_ captura de categoria de PIN**, você pode verificar se ele adicionou o processador de vídeo consultando o Gerenciador de gráfico de filtro para a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="e2f98-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2f98-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2f98-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2f98-110">Capturando vídeo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="e2f98-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



