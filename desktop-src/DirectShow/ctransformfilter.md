---
description: A classe CTransformFilter é uma classe base para implementar filtros de transformação.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: Classe CTransformFilter (Transfrm.h)
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
ms.openlocfilehash: 9d199a406fa1934fb63625cd258baee8d69c20c17992a7d1d3bbd2c83956a1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633886"
---
# <a name="ctransformfilter-class"></a>Classe CTransformFilter

![Hierarquia de classes ctransformfilter](images/tfrm03.png)

A `CTransformFilter` classe é uma classe base para implementar filtros de transformação. Essa classe foi projetada para implementar um filtro de transformação com um pino de entrada e um pino de saída. Ele usa alocadores separados para o pino de entrada e o pino de saída. Para criar um filtro que processa dados no local, use a [**classe CTransInPlaceFilter.**](ctransinplacefilter.md)

Esse filtro usa a [**classe CTransformInputPin para seu**](ctransforminputpin.md) pin de entrada e a classe [**CTransformOutputPin**](ctransformoutputpin.md) para seu pino de saída. Normalmente, você não precisa substituir essas classes de pino. A maioria dos métodos de pino chama métodos correspondentes na classe , para que você possa substituir os métodos `CTransformFilter` de filtro, se necessário. O filtro cria os dois pinos no [**método CTransformFilter::GetPin.**](ctransformfilter-getpin.md) Se você substituir as classes de pino, deverá substituir **GetPin** para criar seus pinos personalizados.

Para usar essa classe, derive uma nova classe de `CTransformFilter` e implemente os seguintes métodos:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter::D eformBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter::Transform**](ctransformfilter-transform.md)

Talvez seja necessário substituir outros métodos também, dependendo dos requisitos do filtro.

## <a name="media-types"></a>Tipos de mídia

O pino de entrada desse filtro não propõe nenhum tipo de mídia; ele se baseia no filtro upstream para propor os tipos de mídia para a conexão. O motivo para esse design é que, na maioria dos casos, o filtro upstream pode fornecer mais informações sobre o formato. Por exemplo, com formatos de vídeo, o filtro upstream conhece as dimensões de vídeo e a taxa de quadros, enquanto o filtro de transformação não tem como determinar essas informações. Se você quiser alterar esse comportamento, substitua o método [**GetMediaType do**](ctransformfilter-getmediatype.md) pino de entrada. Quando o filtro upstream propõe um tipo de mídia, o pino de entrada chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro (virtual puro).

Até que o pino de entrada esteja conectado, o pino de saída recusa todas as conexões e não retorna nenhum tipo de mídia preferencial. Depois que o pino de entrada é conectado, o pino de saída retorna uma lista de tipos preferenciais chamando o [**método GetMediaType do**](ctransformfilter-getmediatype.md) filtro. Ele verifica os tipos de saída para a conexão por meio do método [**CheckTransform do**](ctransformfilter-checktransform.md) filtro. (Ambos os métodos são virtuais puros.) Normalmente, o tipo de entrada determinará parcialmente os tipos de saída aceitáveis.

Dependendo do filtro, talvez você queira registrar alguns dos tipos de mídia com suporte do filtro, para que o objeto [Mapeado](filter-mapper.md) de Filtro possa localizar o filtro. Para obter mais informações, [consulte How to Register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Streaming

Essa classe não enfile os dados de saída. Cada exemplo de saída é entregue dentro [**do método IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) O **método Receive** chama o método [**Transform**](ctransformfilter-transform.md) do filtro (também virtual puro) para processar os dados.

Para obter mais informações sobre como usar essa classe, consulte [Escrevendo filtros de transformação](writing-transform-filters.md).



| Variáveis de membro protegidas                                                | Descrição                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | Sinalizador que indica se o exemplo mais recente foi descartado.                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | Sinalizador que indica se a qualidade foi alterada.                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | Seção crítica que protege o estado do filtro.                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | Seção crítica que protege o estado de streaming.                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | Ponteiro para o pino de entrada.                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | Ponteiro para o pino de saída.                                                                              |
| Métodos públicos                                                            | Descrição                                                                                             |
| [**Ctransformfilter**](ctransformfilter-ctransformfilter.md)             | Método do construtor.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Método destruidor.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Recupera o número de pinos no filtro. Virtual.                                                    |
| [**Getpin**](ctransformfilter-getpin.md)                                 | Recupera um pino. Virtual.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transforma um exemplo de entrada para produzir um exemplo de saída. Virtual.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Chamado quando o filtro alterna para o estado em pausa. Virtual.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Chamado quando o filtro muda para o estado parado. Virtual.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Notifica o filtro de que uma alteração de qualidade é solicitada. Virtual.                                        |
| [**Setmediatype**](ctransformfilter-setmediatype.md)                     | Chamado quando o tipo de mídia é definido em um dos pinos do filtro. Virtual.                                 |
| [**Checkconnect**](ctransformfilter-checkconnect.md)                     | Determina se uma conexão de pino é adequada. Virtual.                                               |
| [**Breakconnect**](ctransformfilter-breakconnect.md)                     | Libera um pin de uma conexão. Virtual.                                                              |
| [**Completeconnect**](ctransformfilter-completeconnect.md)               | Conclui uma conexão de pino. Virtual.                                                                    |
| [**Receber**](ctransformfilter-receive.md)                               | Recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. Virtual. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Recupera um novo exemplo de saída e o inicializa.                                                       |
| [**Endofstream**](ctransformfilter-endofstream.md)                       | Notifica o filtro de que nenhum dado adicional é esperado do pino de entrada. Virtual.                    |
| [**Beginflush**](ctransformfilter-beginflush.md)                         | Inicia uma operação de liberação. Virtual.                                                                      |
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
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




