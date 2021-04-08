---
description: Visão geral da construção de gráficos
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Visão geral da construção de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087554"
---
# <a name="overview-of-graph-building"></a>Visão geral da construção de gráficos

Para criar um gráfico de filtro, comece criando uma instância do Gerenciador do grafo de filtro:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



O Gerenciador de gráficos de filtro dá suporte aos seguintes métodos de construção de grafo:

-   [**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tenta fazer uma conexão direta entre dois Pins. Se os Pins não puderem se conectar, o método falhará.
-   [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta dois Pins. Se possível, ele faz uma conexão direta. Caso contrário, ele usa filtros intermediários para concluir a conexão.
-   [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) inicia a partir de um PIN de saída e compila o restante do grafo. Esse método adiciona filtros conforme necessário, trabalhando downstream, até alcançar um filtro de processador.
-   [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um grafo de reprodução de arquivo completo.
-   [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adiciona um filtro ao grafo. Ele não conecta o filtro. Você deve criar o filtro antes de chamar esse método chamando **CoCreateInstance** ou usando o mapeador de filtro ou o enumerador de dispositivo do sistema.

Esses métodos fornecem três abordagens básicas para criar o grafo:

1.  O Gerenciador de gráfico de filtro cria o grafo inteiro.
2.  O Gerenciador de gráficos de filtro cria parte do grafo.
3.  O aplicativo cria todo o grafo.

**O Gerenciador do grafo de filtro cria o grafo inteiro**

Se você simplesmente deseja reproduzir um arquivo que é criado em um formato reconhecido, como AVI, MPEG, WAV ou MP3, use o método **RenderFile** . O artigo [como reproduzir um arquivo](how-to-play-a-file.md) mostra como fazer isso.

O método **RenderFile** começa examinando o registro de um filtro de origem que pode analisar o arquivo. Ele usa o protocolo (como " `https://` " na URL), a extensão de arquivo ou os padrões de byte predefinidos no arquivo para determinar o filtro de origem. Para obter detalhes, consulte [registrando um tipo de arquivo personalizado](registering-a-custom-file-type.md).

Para compilar o restante do grafo, o Gerenciador de gráficos de filtro usa um processo iterativo em que ele usa os tipos de mídia aos quais um filtro dá suporte em seus PINs de saída e pesquisa o registro em busca de filtros que aceitarão esse tipo de mídia como entrada. Ele usa vários critérios para restringir os filtros de pesquisa e priorização:

-   A *categoria de filtro* identifica a funcionalidade geral do filtro.
-   O tipo de mídia descreve que tipo de dados o filtro pode aceitar como entrada ou entrega como saída.
-   O *mérito* determina a ordem em que os filtros são tentados. Se dois filtros na mesma categoria de filtro oferecerem suporte aos mesmos tipos de entrada, o Gerenciador de gráfico de filtro selecionará aquele com o maior valor de mérito. Alguns filtros são intencionalmente concedidos a um valor de mérito baixo, pois eles são projetados para fins especializados e devem ser adicionados somente ao grafo pelo aplicativo.

O Gerenciador de gráfico de filtro usa o objeto [mapeador de filtro](filter-mapper.md) para pesquisar o registro.

À medida que cada filtro é adicionado, o Gerenciador do grafo de filtro tenta conectá-lo ao pino de saída do filtro anterior. Os filtros negociam para determinar se podem se conectar e, em caso afirmativo, qual tipo de mídia usar para a conexão. Se o novo filtro não puder se conectar, o Gerenciador de gráfico de filtro o descartará e tentará outro filtro. Esse processo continua até que cada fluxo seja renderizado.

**O Gerenciador de gráficos de filtro cria parte do grafo**

Para fazer algo além de simplesmente reproduzir um arquivo, seu aplicativo deve executar pelo menos parte do trabalho de construção do grafo. Por exemplo, um aplicativo de captura de vídeo deve selecionar um filtro de origem de captura e adicioná-lo ao grafo. Se você estiver gravando dados em um arquivo AVI, deverá adicionar os filtros AVI Mux e gravador de arquivo ao grafo. No entanto, muitas vezes é possível deixar o Gerenciador de gráfico de filtro concluir o grafo. Por exemplo, você pode renderizar um PIN para visualização chamando o método **render** .

**O aplicativo cria o grafo inteiro**

Em alguns cenários, seu aplicativo pode precisar criar o grafo adicionando e conectando cada filtro. Nesse caso, você provavelmente saberá especificamente quais filtros devem ser adicionados ao grafo. Com essa abordagem, o aplicativo adiciona cada filtro chamando **AddFilter**, enumera os Pins nos filtros e os conecta chamando **Connect** ou **ConnectDirect**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando gráficos com o construtor de grafo de captura](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Enumerando dispositivos e filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[Criando o grafo de filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



