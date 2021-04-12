---
description: Este tópico descreve como gravar um filtro de origem personalizado para o DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Como escrever um filtro de origem para o DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500667"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Como escrever um filtro de origem para o DirectShow

Este tópico descreve como gravar um filtro de origem personalizado para o DirectShow.

> [!Note]  
> Este tópico descreve somente as fontes push; Ele não descreve fontes de pull, como o filtro de leitor assíncrono ou filtros de Splitter que se conectam a fontes de pull. Para a distinção entre as fontes *Push* e *pull* , consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>O modelo de streaming do DirectShow

Quando você escreve um filtro de origem, é importante entender que uma fonte Push não é a mesma coisa que uma fonte dinâmica. Uma fonte dinâmica obtém dados de alguma fonte externa, como uma câmera ou um fluxo de rede. Geralmente, uma fonte dinâmica não pode controlar a taxa de entrada de dados. Se os filtros downstream não consumirem os dados com rapidez suficiente, a fonte precisará descartar os exemplos.

Mas uma fonte Push não precisa ser uma fonte dinâmica. Por exemplo, uma fonte Push pode ler dados de um arquivo local. Nesse caso, os filtros de renderizador downstream determinam a rapidez com que eles consomem os dados da origem, com base no relógio de referência e nos carimbos de data/hora de exemplo. O filtro de origem fornece amostras o mais rápido possível, mas o fluxo de dados real é restrito pelos renderizadores. Os mecanismos para a retenção do fluxo de dados são descritos em [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).

Cada pino de saída no filtro de origem cria um thread chamado *thread de streaming*. O PIN fornece exemplos no thread de streaming. Normalmente, toda a decodificação, processamento e renderização ocorre nesse thread, embora alguns filtros downstream possam criar threads adicionais para enfileirar suas amostras de saída.

O thread de streaming executa um loop com a seguinte estrutura:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Se não houver amostras disponíveis, a etapa 1 será bloqueada até que um exemplo se torne disponível. A etapa 4 também pode bloquear; por exemplo, ele pode bloquear enquanto o grafo é pausado.

O loop é executado o mais rapidamente possível, mas é limitado pela rapidez com que o filtro de renderizador renderiza cada exemplo. Supondo que o grafo de filtro tenha um relógio de referência, a taxa é determinada pelos tempos de apresentação nos exemplos. Se não houver nenhum relógio de referência, o renderizador consumirá amostras o mais rápido possível.

## <a name="using-csource-and-csourcestream"></a>Usando CSource e CSourceStream

As classes base do DirectShow incluem duas classes que dão suporte a fontes push: [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).

-   [**CSource**](csource.md) é a classe base para o filtro e implementa a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .
-   [**CSourceStream**](csourcestream.md) é a classe base para os Pins de saída e implementa a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

### <a name="output-pins"></a>Pins de saída

Um filtro de origem pode ter mais de um pino de saída. No método do construtor do filtro, crie um ou mais Pins derivados de [**CSourceStream**](csourcestream.md) (um PIN por fluxo de saída). Você não precisa armazenar ponteiros para os Pins; os PINs se adicionam automaticamente ao filtro quando eles são criados.

### <a name="output-formats"></a>Formatos de saída

O pino de saída lida com a negociação de formato com os seguintes métodos [**CSourceStream**](csourcestream.md) :



| Método                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Obtém um tipo de mídia do pino de saída. <br/> O PIN deve propor pelo menos um tipo de mídia, pois o filtro downstream pode não propor nenhum tipo. Na maioria dos casos, o filtro downstream será um decodificador ou um processador, dependendo se o filtro de origem fornece dados compactados ou descompactados. Um filtro de renderizador geralmente requer um tipo de mídia completo, contendo todas as informações de formato necessárias para renderizar o fluxo. Para um decodificador, a quantidade de informações necessárias no tipo de mídia depende muito do formato de codificação.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Verifica se o PIN de saída aceita um determinado tipo de mídia. A substituição desse método é opcional, dependendo de como você implementa [**GetMediaType**](csourcestream-getmediatype.md).                                                                                                                                                                                                                                                                                                                                                                                                         |



 

O método [**GetMediaType**](csourcestream-getmediatype.md) está sobrecarregado:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) usa um único parâmetro, um ponteiro para um objeto [**CMediaType**](cmediatype.md) .
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) pega uma variável de índice e um ponteiro para um objeto [**CMediaType**](cmediatype.md) .

Se o pino de saída do filtro de origem der suporte a exatamente um formato de mídia, você deverá substituir (1) para inicializar o objeto [**CMediaType**](cmediatype.md) com esse formato. Deixe a implementação padrão de (2) e também deixe a implementação padrão de [**CheckMediaType**](csourcestream-checkmediatype.md).

Se o PIN der suporte a mais de um formato, substitua (2). Inicialize o objeto [**CMediaType**](cmediatype.md) de acordo com o valor da variável de índice. O PIN deve retornar os formatos como uma lista ordenada. Nesse caso, você também deve substituir o [**CheckMediaType**](csourcestream-checkmediatype.md) para verificar o tipo de mídia em sua lista de formatos.

Para formatos de vídeo descompactados, lembre-se de que o filtro downstream pode propor formatos com vários valores de Stride. O filtro deve aceitar qualquer valor de Stride válido. Para obter mais informações, consulte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

Você também deve substituir o método puro-virtual [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) . Use esse método para definir o tamanho dos buffers de exemplo.

### <a name="streaming"></a>Streaming

A classe [**CSourceStream**](csourcestream.md) cria o thread de streaming para o PIN. O procedimento de thread é implementado no método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Esse método chama o método puro-virtual [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que a classe derivada deve substituir. Esse método é onde o PIN preenche o buffer com os dados. Por exemplo, se o filtro fornecer vídeo descompactado, é aqui que você desenharia os quadros de vídeo.

A classe base inicia automaticamente e interrompe o loop de thread nos momentos certos, quando o filtro pausa ou para. Quando isso acontece, a classe [**CSourceStream**](csourcestream.md) chama alguns métodos para notificar sua classe derivada:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Você poderá substituir esses métodos se precisar adicionar qualquer manipulação especial. Caso contrário, as implementações padrão simplesmente retornam **S \_ OK**.

## <a name="seeking"></a>Atingir

Se você tiver um filtro de origem com um pino de saída, poderá usar a classe [**CSourceSeeking**](csourceseeking.md) como um ponto de partida para implementar a busca. Herde sua classe PIN de [**CSourceStream**](csourcestream.md) e **CSourceSeeking**.

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) não é recomendado para um filtro com mais de um pino de saída. O principal problema é que apenas um PIN deve responder às solicitações de busca. Normalmente, isso requer a comunicação entre os PINs e o filtro.

 

A classe [**CSourceSeeking**](csourceseeking.md) gerencia a taxa de reprodução, a hora de início, a hora de parada e a duração. Sua classe derivada deve definir a hora de parada inicial e a duração. Sempre que um desses valores é alterado, o método [**CSourceSeeking:: disqueteira**](csourceseeking-changerate.md), [**CSourceSeeking:: altere**](csourceseeking-changestart.md)ou [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md) é chamado, conforme apropriado. Os métodos são todos métodos virtuais puros. A classe de PIN derivada substitui esses métodos para fazer o seguinte:

1.  Chame [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no PIN do downstream. Isso faz com que os filtros downstream liberem amostras que estão mantendo e rejeitam novos exemplos.
2.  Chame [**CSourceStream:: Stop**](csourcestream-stop.md) para interromper o thread de streaming. O filtro de origem suspende a produção de novos dados.
3.  Chame [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no PIN do downstream. Isso sinaliza os filtros downstream para aceitar novos dados.
4.  Chame [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) com as novas horas de início e parada e a taxa.
5.  Defina a propriedade de descontinuidade no próximo exemplo.

Para obter mais informações, consulte [dando suporte à busca em um filtro de origem](supporting-seeking-in-a-source-filter.md).

Se o filtro der suporte à busca, a posição do fluxo agora é independente do tempo de apresentação. Após uma busca, os carimbos de data/hora são redefinidos para zero. A fórmula geral para carimbos de data/hora é:

-   hora de início da amostra = tempo decorrido/taxa de reprodução
-   hora de término da amostra = hora de início da amostra + (hora por período/taxa de reprodução)

Quando o *tempo decorrido* é o tempo decorrido desde que o filtro começou a ser executado ou desde o último comando de busca.

### <a name="time-formats-for-seeking"></a>Formatos de hora para busca

Por padrão, os comandos de busca estão em unidades de 100 a nanossegundos. O filtro de origem pode dar suporte a formatos de tempo adicionais, como busca por número de quadro. Cada formato de hora é identificado por um GUID; consulte [**GUIDs de formato de hora**](time-format-guids.md).

Para dar suporte a formatos de tempo adicionais, você deve implementar os seguintes métodos no seu pino de saída:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Se o aplicativo definir um novo formato de hora, todos os parâmetros de posição nos métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) serão interpretados em termos do novo formato de hora. Por exemplo, se o formato de hora for frames, o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deverá retornar a duração em quadros.

Na prática, alguns filtros do DirectShow dão suporte a formatos de tempo adicionais e, como resultado, alguns aplicativos do DirectShow usam esse recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros de origem](writing-source-filters.md)
</dt> </dl>

 

 




