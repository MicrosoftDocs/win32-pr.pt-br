---
description: Criando gráficos com o construtor de grafo de captura
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Criando gráficos com o construtor de grafo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825986"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>Criando gráficos com o construtor de grafo de captura

Apesar do seu nome, o construtor do grafo de captura é útil para criar muitos tipos de grafos de filtro personalizados, não apenas para capturar grafos. Este artigo fornece uma breve visão geral de como usar esse objeto.

O construtor do grafo de captura expõe a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Comece chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o construtor de grafo de captura e o Gerenciador de gráfico de filtro. Em seguida, inicialize o construtor do grafo de captura chamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) com um ponteiro para o Gerenciador do grafo de filtro, da seguinte maneira:


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>Filtros de conexão

O método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) conecta dois ou três filtros juntos em uma cadeia. Em geral, o método funciona melhor quando cada filtro tem no máximo um PIN de entrada ou um pino de saída do mesmo tipo. Essa discussão começa ignorando os dois primeiros parâmetros de **RenderStream** e concentrando-se nos últimos três parâmetros. O terceiro parâmetro é um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que pode especificar um filtro (como um ponteiro de interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ) ou um pino de saída (como um ponteiro de interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) ). O quarto e o quinto parâmetros especificam ponteiros **IBaseFilter** . O método **RenderStream** conecta todos os três filtros em uma cadeia. Por exemplo, suponha que *A*, *B* e *C* sejam filtros. Suponha que, por enquanto, cada filtro tenha exatamente um PIN de entrada e um pino de saída. A chamada a seguir conecta a a B e, em seguida, B a C:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Todas as conexões são "inteligentes", o que significa que filtros adicionais são adicionados ao grafo, conforme necessário. Para obter detalhes, consulte [conexão inteligente](intelligent-connect.md). Para conectar apenas dois filtros, defina o valor intermediário como **nulo**. Por exemplo, essa chamada conecta a a C:

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

Você pode criar cadeias mais longas chamando o método duas vezes:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Se o último parâmetro for **nulo**, o método localizará automaticamente um renderizador padrão. Ele usa o [processador de vídeo](video-renderer-filter.md) para vídeo e o [renderizador DirectSound](directsound-renderer-filter.md) para áudio. Dessa

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

é equivalente a

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

em que *R* é o renderizador apropriado. Para conectar o filtro de processador de mixagem de vídeo em vez do processador de vídeo, no entanto, você deve especificá-lo explicitamente.

Se você especificar um filtro no terceiro parâmetro, em vez de um PIN, talvez seja necessário indicar qual pino de saída deve ser usado para a conexão. Essa é a finalidade dos dois primeiros parâmetros do método. O primeiro parâmetro se aplica somente a filtros de captura. Especifica um GUID que indica uma categoria de PIN. Para obter uma lista completa de categorias, consulte [Pin Property Set](pin-property-set.md). Duas das categorias são válidas para todos os filtros de captura:

-   **FIXAR \_ captura de categoria \_**
-   **FIXAR \_ Visualização da categoria \_**

Se um filtro de captura não fornecer Pins separados para captura e visualização, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserirá um filtro de " [t" inteligente](smart-tee-filter.md) , que dividirá o fluxo em um fluxo de captura e um fluxo de visualização. Do ponto de vista do aplicativo, você pode simplesmente tratar todos os filtros de captura como tendo os Pins separados e ignorar a topologia subjacente do grafo.

Para a captura de arquivos, conecte o PIN de captura a um filtro Mux. Para a visualização dinâmica, conecte o pino de visualização a um processador. Se você alternar as duas categorias, o grafo poderá remover um número excessivo de quadros durante a captura de arquivo; Mas se o grafo estiver conectado corretamente, ele descartará os quadros de visualização conforme necessário para manter a taxa de transferência no fluxo de captura.

O exemplo a seguir mostra como conectar ambos os fluxos:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Alguns filtros de captura também dão suporte a legendas codificadas, indicadas pela **categoria de PIN \_ \_ VBI**. Para capturar as legendas ocultas em um arquivo, processe essa categoria para o filtro Mux. Para exibir as legendas ocultas na janela de visualização, conecte-se ao renderizador:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



O segundo parâmetro para [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica o tipo de mídia e, normalmente, é um dos seguintes:

-   Áudio de MEDIATYPE \_
-   Vídeo de MEDIATYPE \_
-   MEDIATYPE \_ intercalado (DV)

Você pode usar esse parâmetro sempre que os Pins de saída do filtro suportarem a enumeração de tipos de mídia preferenciais. Para fontes de arquivo, o construtor de grafo de captura adiciona automaticamente um filtro de analisador, se necessário, e, em seguida, consulta os tipos de mídia no analisador. (Para obter um exemplo, consulte [recompactando um arquivo AVI](recompressing-an-avi-file.md).) Além disso, se o último filtro na cadeia tiver vários Pins de entrada, o método tentará enumerar seus tipos de mídia. No entanto, nem todos os filtros dão suporte a essa funcionalidade.

## <a name="finding-interfaces-on-filters-and-pins"></a>Localizando interfaces em filtros e Pins

Depois de criar um grafo, você normalmente precisará localizar várias interfaces expostas por filtros e Pins no grafo. Por exemplo, um filtro de captura pode expor a interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , enquanto os Pins de saída do filtro podem expor a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .

A maneira mais simples de encontrar uma interface é usar o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) . Esse método percorre o grafo (filtros e Pins) até localizar a interface desejada. Você pode especificar o ponto de partida para a pesquisa e pode limitar a pesquisa para filtrar upstream ou downstream a partir do ponto de partida.

O exemplo a seguir pesquisa a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) em um pino de visualização de vídeo:


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> O tópico [Localizar uma interface em um filtro ou PIN](find-an-interface-on-a-filter-or-pin.md) mostra uma abordagem alternativa que usa a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) em vez de [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2). Qual abordagem usar depende do seu aplicativo. Se seu aplicativo já usa **ICaptureGraphBuilder2** para criar o grafo, [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) é uma boa abordagem. Caso contrário, considere o uso dos métodos **IGraphBuilder** .

 

## <a name="finding-pins"></a>Localizando Pins

Com menos frequência, talvez seja necessário localizar um PIN individual em um filtro, embora, na maioria dos casos, os métodos [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) e [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) possam poupar a você o problema. Se você precisar localizar um PIN específico em um filtro, o método auxiliar [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) será útil. Especifique a categoria, o tipo de mídia (vídeo ou áudio), a direção e se o PIN deve ser desconectado.

Por exemplo, o código a seguir procura um PIN de visualização de vídeo desconectado em um filtro de captura:


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
