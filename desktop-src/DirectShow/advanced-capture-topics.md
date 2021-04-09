---
description: Tópicos de captura avançada
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Tópicos de captura avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087788"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="f3a6c-103">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="f3a6c-103">Advanced Capture Topics</span></span>

<span data-ttu-id="f3a6c-104">Esta seção descreve alguns aspectos avançados da captura de vídeo no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="f3a6c-105">A maioria dos problemas descritos nesta seção é manipulada automaticamente pela interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="f3a6c-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="f3a6c-106">No entanto, as informações aqui podem ser úteis se você precisar solucionar problemas de um aplicativo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="f3a6c-107">Você também deve ler esta seção se seu aplicativo criar um grafo de captura personalizado de algum tipo e você achar que o ICaptureGraphBuilder2 não atende às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="f3a6c-108">Por fim, esta seção contém algumas informações sobre como usar o filtro de processador de mixagem de vídeo (VMR) em um aplicativo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="f3a6c-109">É possível criar um grafo de captura de vídeo totalmente usando métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="f3a6c-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="f3a6c-110">Você também pode combinar as duas interfaces, usando ICaptureGraphBuilder2 para algumas tarefas e IGraphBuilder para outras.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="f3a6c-111">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f3a6c-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="f3a6c-112">Manipulando eventos redesenhados na captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f3a6c-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="f3a6c-113">Trabalhando com categorias de PIN</span><span class="sxs-lookup"><span data-stu-id="f3a6c-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="f3a6c-114">Usando o filtro de "t inteligente"</span><span class="sxs-lookup"><span data-stu-id="f3a6c-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="f3a6c-115">Usando o mixer de sobreposição na captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f3a6c-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="f3a6c-116">Pins de porta de vídeo</span><span class="sxs-lookup"><span data-stu-id="f3a6c-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="f3a6c-117">Tipo de formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="f3a6c-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="f3a6c-118">Criando filtros de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="f3a6c-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="f3a6c-119">Filtros de driver de classe WDM</span><span class="sxs-lookup"><span data-stu-id="f3a6c-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="f3a6c-120">Usando a captura do WDDM no DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3a6c-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="f3a6c-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3a6c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3a6c-122">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f3a6c-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



