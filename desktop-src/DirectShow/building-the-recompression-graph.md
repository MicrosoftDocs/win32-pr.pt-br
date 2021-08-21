---
description: Criando a recompactação Graph
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Criando a recompactação Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0432f51e5309a308b32535993fef04da1762d45f179e1ab3a6826d4c5432b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159079"
---
# <a name="building-the-recompression-graph"></a>Criando a recompactação Graph

Um grafo de filtro típico para a recompactação de arquivo AVI é semelhante ao seguinte:

![Grafo de recompactação avi](images/avi2avi4.png)

O [filtro de Splitter AVI](avi-splitter-filter.md) extrai dados do filtro de [origem de arquivo (Async)](file-source--async--filter.md) e os analisa em fluxos de áudio e vídeo. O descompactador de vídeo decodifica o vídeo compactado, onde é recompactado pelo compactador de vídeo. A escolha dos decompactadores depende do arquivo de origem; ele será manipulado automaticamente pelo [Conexão inteligente](intelligent-connect.md). O aplicativo deve escolher o compressor, normalmente apresentando uma lista para o usuário. (Consulte [escolher um filtro de compactação](choosing-a-compression-filter.md).)

Em seguida, o vídeo compactado vai para o [filtro AVI Mux](avi-mux-filter.md). O fluxo de áudio neste exemplo não é compactado, portanto, ele vai diretamente do divisor AVI para o AVI Mux. O AVI Mux intercala os dois fluxos e o filtro do [gravador de arquivo](file-writer-filter.md) grava a saída no disco. Observe que o AVI Mux é necessário mesmo que o arquivo original não tenha um fluxo de áudio.

a maneira mais fácil de criar esse grafo de filtro é usar o [construtor de Graph de captura](capture-graph-builder.md), que é um componente DirectShow para criar grafos de captura e outros gráficos de filtro personalizados.

comece chamando CoCreateInstance para criar o construtor de Graph de captura:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



em seguida, use o construtor de Graph de captura para criar o grafo de filtro:

1.  Crie a seção de renderização do grafo, que inclui o filtro AVI Mux e o [gravador de arquivos](file-writer-filter.md).
2.  Adicione o filtro de origem e o filtro de compactação ao grafo.
3.  Conexão o filtro de origem ao filtro MUX. O construtor de gráficos de captura insere quaisquer filtros de divisor e decodificador necessários para analisar o arquivo de origem. Ele também pode rotear os fluxos de áudio e vídeo por meio de filtros de compactação.

As seções a seguir explicam cada uma dessas etapas.

Criar a seção de renderização

Para criar a seção de renderização do grafo, chame o método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) . Esse método usa parâmetros de entrada que especificam o subtipo de mídia para a saída e o nome do arquivo de saída. Ele retorna ponteiros para o filtro MUX e o gravador de arquivo. O filtro MUX é necessário para o próximo estágio da construção do grafo. O ponteiro para o gravador de arquivo não é necessário para este exemplo, de modo que o parâmetro pode ser **nulo**:


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Quando o método retorna, o filtro MUX tem uma contagem de referência pendente, portanto, certifique-se de liberar o ponteiro mais tarde.

O diagrama a seguir mostra o gráfico de filtro neste ponto.

![seção de renderização do grafo de filtro](images/avi2avi1.png)

O filtro MUX expõe duas interfaces para controlar o formato AVI:

-   [**Interface IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): define o modo de intercalação.
-   [**Interface IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): define o fluxo mestre e o índice de compatibilidade avi.

Adicionar os filtros de origem e de compactação

A próxima etapa é adicionar os filtros de origem e de compactação ao grafo de filtro. o construtor de Graph de captura cria automaticamente uma instância do gerenciador de Graph de filtro quando você chama SetOutputFileName. Obtenha um ponteiro para ele chamando o método [**ICaptureGraphBuilder2:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



Agora, chame o método [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar o filtro de origem de arquivo assíncrono e o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o compressor de vídeo:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



Neste ponto, o filtro de origem e o filtro de compactação não estão conectados a nada mais no grafo, conforme mostrado na ilustração a seguir:

![gráfico de filtro com filtros de origem e de compactação](images/avi2avi2.png)

Conexão a origem ao Mux

A etapa final é conectar o filtro de origem ao filtro AVI Mux por meio do compactador de vídeo. Use o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , que conecta um pino de saída no filtro de origem a um filtro de coletor especificado, opcionalmente por meio de um filtro de compactação.

Os dois primeiros parâmetros especificam qual dos Pins do filtro de origem se conectar, designando uma categoria de PIN e um tipo de mídia. O filtro de origem de arquivo assíncrono tem apenas um pino de saída, portanto, esses parâmetros devem ser **nulos**. Os próximos três parâmetros especificam o filtro de origem, o filtro de compactação (se houver) e o filtro Mux.

O exemplo de código a seguir renderiza a transmissão de vídeo por meio do compactador de vídeo:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



O diagrama a seguir mostra o gráfico de filtro até o momento.

![fluxo de vídeo renderizado](images/avi2avi3.png)

Supondo que o arquivo de origem tenha um fluxo de áudio, o filtro de [Splitter AVI](avi-splitter-filter.md) criou um pino de saída para o áudio. Para conectar esse PIN, chame RenderStream novamente:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



Aqui, nenhum filtro de compactação foi especificado. O pino de saída do filtro de origem já está conectado, portanto, o método RenderStream procura um PIN de saída não conectado no filtro de divisão. Ele encontra o PIN de áudio e o conecta diretamente ao filtro do MUX. Se o arquivo de origem não tiver um fluxo de áudio, a segunda chamada para RenderStream falhará. Esse comportamento é esperado. O grafo é concluído após a primeira chamada para RenderStream, portanto, a falha na segunda chamada é inofensiva.

Neste exemplo, a ordem das duas chamadas RenderStream é importante. Como a segunda chamada não especifica um compressor, ela conectará qualquer PIN não conectado do divisor AVI. Se você fizer essa chamada antes da outra, ela poderá conectar a transmissão de vídeo ao AVI Mux sem o seu compressor de vídeo. Portanto, a chamada mais específica (com o filtro de compactação) deve ocorrer primeiro.

A discussão anterior assumiu que o arquivo de origem é um arquivo AVI. No entanto, essa técnica também funciona com outros tipos de arquivo, como arquivos MPEG. O grafo de filtro resultante será um pouco diferente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recompactando um arquivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 



