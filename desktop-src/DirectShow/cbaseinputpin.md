---
description: A classe CBaseInputPin é uma classe base abstrata para implementar Pins de entrada. Essa classe adiciona suporte para a interface IMemInputPin, além do suporte de interface IPin fornecido pelo CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Classe CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756828"
---
# <a name="cbaseinputpin-class"></a>Classe CBaseInputPin

![hierarquia de classe CBaseInputPin](images/filter07.png)

A `CBaseInputPin` classe é uma classe base abstrata para implementar Pins de entrada. Essa classe adiciona suporte para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , além do suporte de interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) fornecido pelo [**CBasePin**](cbasepin.md).

Para usar essa classe, derive uma nova classe e substitua pelo menos os seguintes métodos:

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin:: receber**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md)

Dependendo da função do PIN, talvez seja necessário substituir métodos adicionais no `CBaseInputPin` ou **CBasePin**.



| Variáveis de membro protegido                                                 | Descrição                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**\_pAllocator m**](cbaseinputpin-m-pallocator.md)                        | Ponteiro para o alocador de memória.                                                                            |
| [**\_bReadOnly m**](cbaseinputpin-m-breadonly.md)                          | Sinalizador que indica se o alocador produz amostras de mídia somente leitura.                                 |
| [**\_bFlushing m**](cbaseinputpin-m-bflushing.md)                          | Sinalizador que indica se o PIN está sendo liberado no momento.                                                  |
| [**\_SampleProps m**](cbaseinputpin-m-sampleprops.md)                      | Propriedades da amostra mais recente.                                                                       |
| Métodos públicos                                                             | Descrição                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Método de construtor.                                                                                         |
| [**~ CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Método destruidor.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Libera o PIN de uma conexão.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Consulta se o alocador usa amostras de mídia somente leitura.                                                 |
| [**Islibere**](cbaseinputpin-isflushing.md)                             | Consulta se o filtro está sendo liberado no momento.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Determina se o PIN pode aceitar amostras. VirtuaisLUNs.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Passa uma mensagem de controle de qualidade para o objeto apropriado.                                                 |
| [**Inativo**](cbaseinputpin-inactive.md)                                 | Notifica o PIN de que o filtro não está mais ativo. VirtuaisLUNs.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Recupera as propriedades do exemplo mais recente.                                                         |
| Métodos IPin                                                               | Descrição                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Inicia uma operação de liberação.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Finaliza uma operação de liberação.                                                                                     |
| Métodos IMemInputPin                                                       | Descrição                                                                                                 |
| [**Getalocador**](cbaseinputpin-getallocator.md)                         | Recupera o alocador de memória proposto por este pin.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Especifica um alocador para a conexão.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Recupera as propriedades de alocador solicitadas pelo pino de entrada.                                              |
| [**Recebe**](cbaseinputpin-receive.md)                                   | Recebe o próximo exemplo de mídia no fluxo.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Recebe vários exemplos no fluxo.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Determina se as chamadas para o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) podem ser bloqueadas. |
| Métodos IQualityControl                                                    | Descrição                                                                                                 |
| [**Notificar**](cbaseinputpin-notify.md)                                     | Recebe uma mensagem de controle de qualidade.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




