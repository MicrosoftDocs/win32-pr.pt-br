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
# <a name="about-the-capture-graph-builder"></a>Sobre o construtor do grafo de captura

Um grafo de filtro que executa a captura de vídeo ou áudio é chamado de *grafo de captura*. Gráficos de captura geralmente são mais complicados do que os grafos de reprodução de arquivos. Para tornar mais fácil para os aplicativos criar grafos de captura, o DirectShow fornece um objeto auxiliar chamado Construtor de gráficos de captura. O construtor de grafo de captura expõe a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , que contém métodos para criar e controlar um grafo de captura. O diagrama a seguir ilustra o construtor de grafo de captura e a interface **ICaptureGraphBuilder2** .

![usando o construtor de grafo de captura](images/cgb01.png)

Comece chamando CoCreateInstance para criar novas instâncias do construtor de grafo de captura e do Gerenciador de gráfico de filtro. Em seguida, inicialize o construtor do grafo de captura chamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) com um ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do Gerenciador do grafo de filtro. O diagrama a seguir ilustra esse processo.

![Inicializando o construtor do grafo de captura](images/cgb03.png)

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



Ao longo desta seção sobre a captura de vídeo, supõe-se que você esteja usando o construtor de grafo de captura para criar o grafo de captura. No entanto, é possível criar gráficos de captura totalmente usando métodos IGraphBuilder. Isso é considerado um tópico avançado, no entanto, e os métodos do construtor do grafo de captura são preferenciais. Para obter mais informações, consulte [Tópicos de captura avançada](advanced-capture-topics.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a captura de vídeo no DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



