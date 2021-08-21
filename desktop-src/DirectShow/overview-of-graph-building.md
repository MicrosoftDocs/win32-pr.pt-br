---
description: Visão geral do Graph Building
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Visão geral do Graph Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16b943714e2e559286b805a8489152805d9b0e037a77603bacd00f8b0135cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152942"
---
# <a name="overview-of-graph-building"></a>Visão geral do Graph Building

Para criar um grafo de filtro, comece criando uma instância do Gerenciador Graph Filtro:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



O Gerenciador Graph Filtro dá suporte aos seguintes métodos de criação de grafo:

-   [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tenta fazer uma conexão direta entre dois pinos. Se os pinos não puderem se conectar, o método falhará.
-   [**IGraphBuilder::Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta dois pinos. Se possível, ele faz uma conexão direta. Caso contrário, ele usará filtros intermediários para concluir a conexão.
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) começa em um pino de saída e cria o restante do grafo. Esses métodos adicionam filtros conforme necessário, trabalhando downstream até atingir um filtro do renderador.
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um grafo de reprodução de arquivo completo.
-   [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adiciona um filtro ao grafo. Ele não conecta o filtro. Você deve criar o filtro antes de chamar esse método, chamando **CoCreateInstance** ou usando o Mapeador de Filtros ou o Enumerador de Dispositivo do Sistema.

Esses métodos fornecem três abordagens básicas para criar o grafo:

1.  O Gerenciador Graph Filtro cria todo o grafo.
2.  O Gerenciador Graph Filtro cria parte do grafo.
3.  O aplicativo cria todo o grafo.

**O gerenciador Graph filtro cria o Graph**

Se você simplesmente quiser reproduzir um arquivo que é autor em um formato reconhecido, como AVI, MPEG, WAV ou MP3, use o **método RenderFile.** O artigo [How To Play a File](how-to-play-a-file.md) mostra como fazer isso.

O **método RenderFile** começa procurando no Registro um filtro de origem que possa analisar o arquivo. Ele usa o protocolo (como " " na URL), a extensão de arquivo ou padrões de byte pré-definidos no arquivo para `https://` determinar o filtro de origem. Para obter detalhes, [consulte Registrando um tipo de arquivo personalizado](registering-a-custom-file-type.md).

Para criar o restante do grafo, o Gerenciador de filtros Graph usa um processo iterativo em que usa os tipos de mídia aos quais um filtro dá suporte em seus pinos de saída e pesquisa no Registro filtros que aceitarão esse tipo de mídia como entrada. Ele usa vários critérios para restringir a pesquisa e priorizar filtros:

-   A *categoria de* filtro identifica a funcionalidade geral do filtro.
-   O tipo de mídia descreve que tipo de dados o filtro pode aceitar como entrada ou entrega como saída.
-   O *valor* determina a ordem em que os filtros são tentados. Se dois filtros na mesma categoria de filtros deem suporte aos mesmos tipos de entrada, o Gerenciador de Graph de Filtros selecionará aquele com o valor de maior valor de prêmio. Alguns filtros têm um valor baixo porque foram projetados para fins especializados e só devem ser adicionados ao grafo pelo aplicativo.

O Gerenciador Graph Filtro usa o [objeto Mapeado de](filter-mapper.md) Filtro para pesquisar o Registro.

À medida que cada filtro é adicionado, o Gerenciador Graph filtro tenta conectá-lo ao pino de saída do filtro anterior. Os filtros negociam para determinar se eles podem se conectar e, nesse caso, qual tipo de mídia usar para a conexão. Se o novo filtro não puder se conectar, o Gerenciador Graph Filtro o descartará e tentará outro filtro. Esse processo continua até que cada fluxo seja renderizado.

**O gerenciador Graph filtro cria parte do Graph**

Para fazer algo além de simplesmente executar um arquivo, seu aplicativo deve executar pelo menos parte do trabalho de criação de grafo. Por exemplo, um aplicativo de captura de vídeo deve selecionar um filtro de origem de captura e adicioná-lo ao grafo. Se você estiver escrevendo dados em um arquivo AVI, deverá adicionar os filtros AVI Mux e File Writer ao grafo. No entanto, geralmente é possível permitir que o Gerenciador Graph Filtro conclua o grafo. Por exemplo, você pode renderizar um pin para visualização chamando o **método Renderizar.**

**O aplicativo cria toda a Graph**

Em alguns cenários, seu aplicativo pode precisar criar o grafo adicionando e conectando cada filtro. Nesse caso, você provavelmente sabe especificamente quais filtros devem ser adicionados ao grafo. Com essa abordagem, o aplicativo adiciona cada filtro chamando **AddFilter**, enumera os pinos nos filtros e os conecta chamando Conexão **ou** **ConnectDirect**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando grafos com o Construtor de Graph De captura](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Enumerando dispositivos e filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerando objetos em um filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Técnicas Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[Criando o filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



