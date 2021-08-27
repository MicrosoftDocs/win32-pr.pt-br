---
description: Sobre o Capture Graph Builder
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Sobre o Capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ef82a160ada6e53fe6d2db830efa85118eb699074630905cd41f0b5412ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664505"
---
# <a name="about-the-capture-graph-builder"></a>Sobre o Capture Graph Builder

Um grafo de filtro que executa a captura de áudio ou vídeo é chamado de *grafo de captura*. Os grafos de captura geralmente são mais complicados do que os grafos de reprodução de arquivo. Para facilitar a com que os aplicativos criem grafos de captura, DirectShow fornece um objeto auxiliar chamado Capture Graph Builder. O Construtor Graph Capture expõe a interface [**ICaptureGraphBuilder2,**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) que contém métodos para criar e controlar um grafo de captura. O diagrama a seguir ilustra o Capture Graph Builder e a interface **ICaptureGraphBuilder2.**

![usando o construtor de grafo de captura](images/cgb01.png)

Comece chamando CoCreateInstance para criar novas instâncias do Capture Graph Builder e do Gerenciador de Graph Filtro. Em seguida, inicialize o Capture Graph Builder chamando [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) com um ponteiro para Graph a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do Gerenciador de Filtros. O diagrama a seguir ilustra esse processo.

![inicializando o construtor de grafo de captura](images/cgb03.png)

O código a seguir mostra uma função auxiliar para executar estas etapas:


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



Ao longo desta seção sobre captura de vídeo, supõe-se que você está usando o Capture Graph Builder para criar o grafo de captura. No entanto, é possível criar grafos de captura inteiramente usando métodos IGraphBuilder. No entanto, isso é considerado um tópico avançado e os métodos capture Graph Builder são preferenciais. Para obter mais informações, consulte [Tópicos de captura avançada.](advanced-capture-topics.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a Captura de Vídeo DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



