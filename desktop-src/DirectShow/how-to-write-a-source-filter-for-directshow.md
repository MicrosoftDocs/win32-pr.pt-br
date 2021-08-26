---
description: Este tópico descreve como escrever um filtro de origem personalizado para DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Como escrever um filtro de origem para DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ea6821dc7d56f2628ce68e7320e5e76b2c1643978e68287d434b7a111cbbd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043236"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Como escrever um filtro de origem para DirectShow

Este tópico descreve como escrever um filtro de origem personalizado para DirectShow.

> [!Note]  
> Este tópico descreve apenas fontes push; ele não descreve fontes de pull, como o Filtro de Leitor Assíncrono ou filtros divisor que se conectam a fontes de pull. Para ver a distinção *entre as fontes push* e *pull,* consulte [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>O modelo DirectShow streaming

Quando você escreve um filtro de origem, é importante entender que uma fonte de push não é a mesma coisa que uma fonte ao vivo. Uma fonte ao vivo obtém dados de alguma fonte externa, como uma câmera ou um fluxo de rede. Em geral, uma fonte ao vivo não pode controlar a taxa de entrada de dados. Se os filtros downstream não consumirem os dados com rapidez suficiente, a origem precisará soltar amostras.

Mas uma fonte de push não precisa ser uma fonte ao vivo. Por exemplo, uma fonte push pode ler dados de um arquivo local. Nesse caso, os filtros do renderador downstream determinam a velocidade com que eles consomem os dados da origem, com base no relógio de referência e nos carimbos de data/hora de exemplo. O filtro de origem fornece amostras o mais rápido possível, mas o fluxo de dados real é limitado pelos renderadores. Os mecanismos para a proteção do fluxo de dados são descritos em [Data Flow para desenvolvedores de filtro.](data-flow-for-filter-developers.md)

Cada pino de saída no filtro de origem cria um thread chamado *thread de streaming*. O pino fornece exemplos no thread de streaming. Normalmente, toda a decodificação, o processamento e a renderização ocorrem nesse thread, embora alguns filtros downstream possam criar threads adicionais para enfilar seus exemplos de saída.

O thread de streaming executa um loop com a seguinte estrutura:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Se nenhum exemplo estiver disponível, a etapa 1 bloqueará até que uma amostra fique disponível. A etapa 4 também pode bloquear; por exemplo, ele pode bloquear enquanto o grafo está em pausa.

O loop é executado o mais rápido possível, mas é limitado pela rapidez com que o filtro de renderização renderiza cada amostra. Supondo que o grafo de filtro tenha um relógio de referência, a taxa é determinada pelos tempos de apresentação nos exemplos. Se não houver relógio de referência, o renderista consumirá amostras o mais rápido possível.

## <a name="using-csource-and-csourcestream"></a>Usando CSource e CSourceStream

As DirectShow base incluem duas classes que suportam fontes push: [**CSource**](csource.md) e [**CSourceStream.**](csourcestream.md)

-   [**CSource é**](csource.md) a classe base para o filtro e implementa a interface [**IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)
-   [**CSourceStream**](csourcestream.md) é a classe base para os pinos de saída e implementa a interface [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

### <a name="output-pins"></a>Pinos de saída

Um filtro de origem pode ter mais de um pino de saída. No método de construtor do filtro, crie um ou mais pinos derivados de [**CSourceStream**](csourcestream.md) (um pino por fluxo de saída). Você não precisa armazenar ponteiros para os pinos; os pinos se adicionam automaticamente ao filtro quando são criados.

### <a name="output-formats"></a>Formatos de saída

O pino de saída lida com a negociação de formato com os [**seguintes métodos CSourceStream:**](csourcestream.md)



| Método                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getmediatype**](csourcestream-getmediatype.md)     | Obtém um tipo de mídia do pino de saída. <br/> O pino deve propor pelo menos um tipo de mídia, pois o filtro downstream pode não propor nenhum tipo. Na maioria dos casos, o filtro downstream será um decodificador ou um renderdor, dependendo se o filtro de origem entregar dados compactados ou descompactados. Um filtro de renderização geralmente requer um tipo de mídia completo, contendo todas as informações de formato necessárias para renderizar o fluxo. Para um decodificador, a quantidade de informações necessárias no tipo de mídia depende muito do formato de codificação.<br/> |
| [**Checkmediatype**](csourcestream-checkmediatype.md) | Verifica se o pino de saída aceita um determinado tipo de mídia. A substituição desse método é opcional, dependendo de como você implementa [**GetMediaType**](csourcestream-getmediatype.md).                                                                                                                                                                                                                                                                                                                                                                                                         |



 

O [**método GetMediaType**](csourcestream-getmediatype.md) está sobrecarregado:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) aceita um único parâmetro, um ponteiro para um [**objeto CMediaType.**](cmediatype.md)
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) leva uma variável de índice e um ponteiro para um [**objeto CMediaType.**](cmediatype.md)

Se o pino de saída do filtro de origem for compatível com exatamente um formato de mídia, você deverá substituir (1) para inicializar o [**objeto CMediaType**](cmediatype.md) com esse formato. Deixe a implementação padrão de (2) e também deixe a implementação padrão de [**CheckMediaType.**](csourcestream-checkmediatype.md)

Se o pino for compatível com mais de um formato, substitua (2). Inicialize o [**objeto CMediaType**](cmediatype.md) de acordo com o valor da variável de índice. O pino deve retornar os formatos como uma lista ordenada. Nesse caso, você também deve substituir [**o CheckMediaType**](csourcestream-checkmediatype.md) para verificar o tipo de mídia em relação à sua lista de formatos.

Para formatos de vídeo descompactados, lembre-se de que o filtro downstream pode propor formatos com vários valores de stride. Seu filtro deve aceitar qualquer valor de stride válido. Para obter mais informações, [**consulte BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

Você também deve substituir o método [**CBaseOutputPin::D eputaçãoBufferSize**](cbaseoutputpin-decidebuffersize.md) puramente virtual. Use esse método para definir o tamanho dos buffers de exemplo.

### <a name="streaming"></a>Streaming

A [**classe CSourceStream**](csourcestream.md) cria o thread de streaming para o pino. O procedimento de thread é implementado no [**método CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Esse método chama o método [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) puro-virtual, que a classe derivada deve substituir. Esse método é onde o pino preenche o buffer com dados. Por exemplo, se o filtro entregar um vídeo descompactado, você desenhará os quadros de vídeo.

A classe base inicia e interrompe automaticamente o loop de thread nos momentos certos, quando o filtro pausa ou para. Quando isso acontece, a [**classe CSourceStream**](csourcestream.md) chama alguns métodos para notificar sua classe derivada:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Você poderá substituir esses métodos se precisar adicionar qualquer manipulação especial. Caso contrário, as implementações padrão simplesmente retornarão **S \_ OK.**

## <a name="seeking"></a>Procurando

Se você tiver um filtro de origem com um pino de saída, poderá usar a [**classe CSourceSeeking**](csourceseeking.md) como um ponto de partida para implementar a busca. Herde sua classe de pino [**de CSourceStream**](csourcestream.md) e **CSourceSeeking.**

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) não é recomendado para um filtro com mais de um pino de saída. O principal problema é que apenas um pino deve responder às solicitações de busca. Normalmente, isso requer comunicação entre os pinos e o filtro.

 

A [**classe CSourceSeeking**](csourceseeking.md) gerencia a taxa de reprodução, a hora de início, a hora de parada e a duração. Sua classe derivada deve definir o tempo de parada inicial e a duração. Sempre que um desses valores mudar, o método [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md), [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)ou [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md) será chamado, conforme apropriado. Os métodos são todos métodos virtuais puros. A classe de pino derivada substitui esses métodos para fazer o seguinte:

1.  Chame [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino downstream. Isso faz com que os filtros downstream liberem exemplos que estão mantendo e rejeitem novas amostras.
2.  Chame [**CSourceStream::Stop para**](csourcestream-stop.md) interromper o thread de streaming. O filtro de origem suspende a produção de novos dados.
3.  Chame [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino downstream. Isso sinaliza os filtros downstream para aceitar novos dados.
4.  Chame [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) com os novos horários de início e parada e a taxa.
5.  De definir a propriedade de descontinuidade no próximo exemplo.

Para obter mais informações, consulte [Suporte à busca em um filtro de origem](supporting-seeking-in-a-source-filter.md).

Se o filtro dá suporte à busca, a posição do fluxo agora é independente do tempo de apresentação. Após uma busca, os carimbos de data/hora são redefinidos como zero. A fórmula geral para carimbos de data/hora é:

-   hora de início de exemplo = tempo decorrido/taxa de reprodução
-   sample end time = sample start time + (time per frame/playback rate)

em *que o tempo decorrido* é o tempo decorrido desde que o filtro começou a ser executado ou desde o último comando de busca.

### <a name="time-formats-for-seeking"></a>Formatos de tempo para busca

Por padrão, os comandos de busca estão em unidades de 100 a nanossegundos. O filtro de origem pode dar suporte a formatos de tempo adicionais, como busca por número de quadro. Cada formato de hora é identificado por um GUID; consulte [**GUIDs de formato de hora**](time-format-guids.md).

Para dar suporte a formatos de tempo adicionais, você deve implementar os seguintes métodos no seu pino de saída:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Se o aplicativo definir um novo formato de hora, todos os parâmetros de posição nos métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) serão interpretados em termos do novo formato de hora. Por exemplo, se o formato de hora for frames, o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deverá retornar a duração em quadros.

na prática, alguns filtros de DirectShow dão suporte a formatos de tempo adicionais e, como resultado, alguns aplicativos de DirectShow usam esse recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros de origem](writing-source-filters.md)
</dt> </dl>

 

 




