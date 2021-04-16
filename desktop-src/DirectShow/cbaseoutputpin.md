---
description: A classe CBaseOutputPin é uma classe base abstrata que implementa um pino de saída.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Classe CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750067"
---
# <a name="cbaseoutputpin-class"></a>Classe CBaseOutputPin

![hierarquia de classe CBaseOutputPin](images/filter06.png)

A `CBaseOutputPin` classe é uma classe base abstrata que implementa um pino de saída.

Essa classe deriva de [**CBasePin**](cbasepin.md). Ele difere do **CBasePin** nos seguintes aspectos:

-   Ele se conecta somente a Pins de entrada que dão suporte à interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Ele dá suporte ao transporte de memória local por meio da interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .
-   Ele rejeita as notificações de fim de fluxo, liberação e novo segmento. (Eles não devem ser enviados a um PIN de saída.)
-   Ele fornece métodos para a distribuição de amostras downstream.

Quando o PIN se conecta, ele solicita um alocador de memória do PIN de entrada. Falhando, ele cria um novo objeto de alocador. O pino de saída é responsável por definir as propriedades do alocador. Ele faz isso por meio do método virtual puro [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md). Substitua esse método em sua classe derivada. Se o pino de entrada tiver requisitos de buffer, eles serão passados para o método **DecideBufferSize** .

Chame o método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obter um exemplo de mídia vazio. Chame o método [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) para entregar amostras downstream.

Sua classe derivada deve substituir o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) puro virtual para validar o tipo de mídia durante conexões de PIN.



| Variáveis de membro protegido                                      | Descrição                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**\_pAllocator m**](cbaseoutputpin-m-pallocator.md)            | Ponteiro para o alocador de memória.                                           |
| [**\_pInputPin m**](cbaseoutputpin-m-pinputpin.md)              | Ponteiro para o pino de entrada conectado a este pin.                            |
| Métodos públicos                                                  | Descrição                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Método de construtor.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Conclui uma conexão com um PIN de entrada. VirtuaisLUNs.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Seleciona um alocador de memória. VirtuaisLUNs.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Recupera um exemplo de mídia que contém um buffer vazio. VirtuaisLUNs.           |
| [**Fornecimento**](cbaseoutputpin-deliver.md)                       | Entrega um exemplo de mídia para o pino de entrada conectado. VirtuaisLUNs.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Cria um alocador de memória. VirtuaisLUNs.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Determina se uma conexão de PIN é adequada.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Libera o PIN de uma conexão.                                        |
| [**Activo**](cbaseoutputpin-active.md)                         | Notifica o PIN de que o filtro está ativo agora.                            |
| [**Inativo**](cbaseoutputpin-inactive.md)                     | Notifica o PIN de que o filtro não está mais ativo.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Entrega uma notificação de fim de fluxo para o PIN de entrada conectado. VirtuaisLUNs. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Solicita que o PIN de entrada conectado inicie uma operação de liberação. VirtuaisLUNs.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Solicita que o PIN de entrada conectado Finalize uma operação de liberação. VirtuaisLUNs.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Entrega uma notificação de novo segmento para o PIN de entrada conectado. VirtuaisLUNs.   |
| Métodos virtuais puros                                            | Descrição                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Define os requisitos de buffer.                                              |
| Métodos IPin                                                    | Descrição                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Inicia uma operação de liberação.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Finaliza uma operação de liberação.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Notifica o PIN de que nenhum dado adicional é esperado.                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




