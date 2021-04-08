---
description: Sobre o construtor do grafo de captura
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Sobre o construtor do grafo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920024"
---
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="fabe2-103">Sobre o construtor do grafo de captura</span><span class="sxs-lookup"><span data-stu-id="fabe2-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="fabe2-104">Um grafo de filtro que executa a captura de vídeo ou áudio é chamado de *grafo de captura*.</span><span class="sxs-lookup"><span data-stu-id="fabe2-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="fabe2-105">Gráficos de captura geralmente são mais complicados do que os grafos de reprodução de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fabe2-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="fabe2-106">Para tornar mais fácil para os aplicativos criar grafos de captura, o DirectShow fornece um objeto auxiliar chamado Construtor de gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="fabe2-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="fabe2-107">O construtor de grafo de captura expõe a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , que contém métodos para criar e controlar um grafo de captura.</span><span class="sxs-lookup"><span data-stu-id="fabe2-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="fabe2-108">O diagrama a seguir ilustra o construtor de grafo de captura e a interface **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="fabe2-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![usando o construtor de grafo de captura](images/cgb01.png)

<span data-ttu-id="fabe2-110">Comece chamando CoCreateInstance para criar novas instâncias do construtor de grafo de captura e do Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fabe2-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="fabe2-111">Em seguida, inicialize o construtor do grafo de captura chamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) com um ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="fabe2-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="fabe2-112">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="fabe2-112">The following diagram illustrates this process.</span></span>

![Inicializando o construtor do grafo de captura](images/cgb03.png)

<span data-ttu-id="fabe2-114">O código a seguir mostra uma função auxiliar para executar estas etapas:</span><span class="sxs-lookup"><span data-stu-id="fabe2-114">The following code shows a helper function to perform these steps:</span></span>


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



<span data-ttu-id="fabe2-115">Ao longo desta seção sobre a captura de vídeo, supõe-se que você esteja usando o construtor de grafo de captura para criar o grafo de captura.</span><span class="sxs-lookup"><span data-stu-id="fabe2-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="fabe2-116">No entanto, é possível criar gráficos de captura totalmente usando métodos IGraphBuilder.</span><span class="sxs-lookup"><span data-stu-id="fabe2-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="fabe2-117">Isso é considerado um tópico avançado, no entanto, e os métodos do construtor do grafo de captura são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="fabe2-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="fabe2-118">Para obter mais informações, consulte [Tópicos de captura avançada](advanced-capture-topics.md).</span><span class="sxs-lookup"><span data-stu-id="fabe2-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fabe2-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fabe2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fabe2-120">Sobre a captura de vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="fabe2-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



