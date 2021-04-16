---
description: A classe CTransformFilter é uma classe base para implementar filtros de transformação.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: Classe CTransformFilter (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d24c305b28641fcee366b4e906b87008decac014
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750651"
---
# <a name="ctransformfilter-class"></a>Classe CTransformFilter

![hierarquia de classe CTransformFilter](images/tfrm03.png)

A `CTransformFilter` classe é uma classe base para implementar filtros de transformação. Essa classe foi projetada para implementar um filtro de transformação com um PIN de entrada e um PIN de saída. Ele usa alocadores separados para o pino de entrada e o pino de saída. Para criar um filtro que processa dados no local, use a classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Esse filtro usa a classe [**CTransformInputPin**](ctransforminputpin.md) para seu pino de entrada e a classe [**CTransformOutputPin**](ctransformoutputpin.md) para seu pino de saída. Normalmente, você não precisa substituir essas classes de PIN. A maioria dos métodos de fixação chamam os métodos correspondentes na `CTransformFilter` classe, para que você possa substituir os métodos de filtro, se necessário. O filtro cria ambos os Pins no método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) . Se você substituir as classes de PIN, deverá substituir **GetPin** para criar seus PINs personalizados.

Para usar essa classe, derive uma nova classe de `CTransformFilter` e implemente os seguintes métodos:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter:: Transform**](ctransformfilter-transform.md)

Talvez seja necessário substituir outros métodos também, dependendo dos requisitos do seu filtro.

## <a name="media-types"></a>Tipos de mídia

O PIN de entrada do filtro não propõe nenhum tipo de mídia; Ele depende do filtro upstream para propor os tipos de mídia para a conexão. O motivo para esse design é que, na maioria dos casos, o filtro upstream pode fornecer mais informações sobre o formato. Por exemplo, com formatos de vídeo, o filtro upstream conhece as dimensões de vídeo e a taxa de quadros, enquanto o filtro de transformação não tem como determinar essas informações. Se você quiser alterar esse comportamento, substitua o método [**GetMediaType**](ctransformfilter-getmediatype.md) do pino de entrada. Quando o filtro upstream propõe um tipo de mídia, o pino de entrada chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro (virtual puro).

Até que o pino de entrada seja conectado, o PIN de saída recusará todas as conexões e não retornará nenhum tipo de mídia preferencial. Depois que o pino de entrada é conectado, o pino de saída retorna uma lista de tipos preferenciais chamando o método [**GetMediaType**](ctransformfilter-getmediatype.md) do filtro. Ele verifica os tipos de saída para a conexão por meio do método [**CheckTransform**](ctransformfilter-checktransform.md) do filtro. (Ambos os métodos são virtuais puros.) Normalmente, o tipo de entrada determinará, parcialmente, os tipos de saída aceitáveis.

Dependendo do filtro, talvez você queira registrar alguns dos tipos de mídia com suporte do filtro, para que o objeto [mapeador de filtro](filter-mapper.md) possa localizar o filtro. Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Streaming

Essa classe não enfileira os dados de saída. Cada exemplo de saída é entregue dentro do método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) . O método **Receive** chama o método [**Transform**](ctransformfilter-transform.md) do filtro (também virtual puro) para processar os dados.

Para obter mais informações sobre como usar essa classe, consulte [Writing Transform Filters](writing-transform-filters.md).



| Variáveis de membro protegido                                                | Descrição                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**\_bEOSDelivered m**](ctransformfilter-m-beosdelivered.md)              | Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.                          |
| [**\_bSampleSkipped m**](ctransformfilter-m-bsampleskipped.md)            | Sinalizador que indica se a amostra mais recente foi descartada.                                         |
| [**\_bQualityChanged m**](ctransformfilter-m-bqualitychanged.md)          | Sinalizador que indica se a qualidade foi alterada.                                                    |
| [**\_csFilter m**](ctransformfilter-m-csfilter.md)                        | Seção crítica que protege o estado do filtro.                                                        |
| [**\_csReceive m**](ctransformfilter-m-csreceive.md)                      | Seção crítica que protege o estado de streaming.                                                     |
| [**\_pInput m**](ctransformfilter-m-pinput.md)                            | Ponteiro para o pino de entrada.                                                                               |
| [**\_pOutput m**](ctransformfilter-m-poutput.md)                          | Ponteiro para o pino de saída.                                                                              |
| Métodos públicos                                                            | Descrição                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | Método de construtor.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Método destruidor.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Recupera o número de Pins no filtro. VirtuaisLUNs.                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | Recupera um PIN. VirtuaisLUNs.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transforma um exemplo de entrada para produzir um exemplo de saída. VirtuaisLUNs.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Chamado quando o filtro alterna para o estado pausado. VirtuaisLUNs.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Chamado quando o filtro alterna para o estado parado. VirtuaisLUNs.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Notifica o filtro de que uma alteração de qualidade é solicitada. VirtuaisLUNs.                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | Chamado quando o tipo de mídia é definido em um dos Pins do filtro. VirtuaisLUNs.                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | Determina se uma conexão de PIN é adequada. VirtuaisLUNs.                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | Libera um PIN de uma conexão. VirtuaisLUNs.                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | Conclui uma conexão de PIN. VirtuaisLUNs.                                                                    |
| [**Recebe**](ctransformfilter-receive.md)                               | Recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. VirtuaisLUNs. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Recupera um novo exemplo de saída e inicializa-o.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Notifica o filtro de que nenhum dado adicional é esperado do pino de entrada. VirtuaisLUNs.                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | Inicia uma operação de liberação. VirtuaisLUNs.                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | Finaliza uma operação de liberação. VirtuaisLUNs.                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | Notifica o filtro que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento. VirtuaisLUNs.      |
| Métodos virtuais puros                                                      | Descrição                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | Verifica se um tipo de mídia especificado é aceitável para entrada.                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | Verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | Define os requisitos de buffer do pino de saída.                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | Recupera um tipo de mídia preferencial para o pino de saída.                                                    |
| Métodos IMediaFilter                                                      | Descrição                                                                                             |
| [**Stop**](ctransformfilter-stop.md)                                     | Interrompe o filtro.                                                                                       |
| [**Pausar**](ctransformfilter-pause.md)                                   | Pausa o filtro.                                                                                      |
| Métodos IBaseFilter                                                       | Descrição                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | Recupera o PIN com o identificador especificado.                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




