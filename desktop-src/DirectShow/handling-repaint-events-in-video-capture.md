---
description: Manipulando eventos redesenhados na captura de vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Manipulando eventos redesenhados na captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920047"
---
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="1b383-103">Manipulando eventos redesenhados na captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="1b383-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="1b383-104">Se você criar um grafo de captura de vídeo sem usar a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) e visualizar o vídeo usando o filtro antigo de processamento de vídeo, deverá substituir o tratamento padrão para [**eventos \_ Repaints do EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="1b383-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="1b383-105">Consulte o Gerenciador do grafo de filtro para a interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) e chame o método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) com o valor EC \_ Repaint:</span><span class="sxs-lookup"><span data-stu-id="1b383-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="1b383-106">Isso impede um possível erro que pode corromper o arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="1b383-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="1b383-107">Se o usuário cobrir e descobrir a janela de visualização, o filtro de processamento de vídeo receberá uma mensagem de pintura do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="1b383-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="1b383-108">Por padrão, o processador de vídeo solicita um novo quadro e o Gerenciador de gráficos de filtro pausa o grafo para marcar outro quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b383-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="1b383-109">Se isso acontecer enquanto o grafo estiver gravando um arquivo, ele corromperá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b383-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="1b383-110">Substituir o comportamento padrão de \_ redesenho do EC impede que o renderizador solicite um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="1b383-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="1b383-111">Você não precisará executar esta etapa se estiver usando a interface **ICaptureGraphBuilder2** , pois o construtor do grafo de captura faz isso para você automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1b383-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="1b383-112">Além disso, ele não será necessário se você estiver usando o VMR (processador de mixagem de vídeo) para visualização.</span><span class="sxs-lookup"><span data-stu-id="1b383-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="1b383-113">O VMR sempre tem o quadro mais recente disponível, portanto, não envia eventos de \_ redesenho de EC.</span><span class="sxs-lookup"><span data-stu-id="1b383-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b383-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b383-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b383-115">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="1b383-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="1b383-116">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b383-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



