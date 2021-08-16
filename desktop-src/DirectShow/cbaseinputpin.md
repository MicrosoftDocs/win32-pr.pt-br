---
description: A classe CBaseInputPin é uma classe base abstrata para implementar pinos de entrada. Essa classe adiciona suporte para a interface IMemInputPin, além do suporte à interface IPin fornecido pelo CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Classe CBaseInputPin (Amfilter.h)
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
ms.openlocfilehash: ab98a2dcb1503e7593912df0e5dff51539855611311d4704e4045816fd6380e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823876"
---
# <a name="cbaseinputpin-class"></a>Classe CBaseInputPin

![Hierarquia de classes cbaseinputpin](images/filter07.png)

A `CBaseInputPin` classe é uma classe base abstrata para implementar pinos de entrada. Essa classe adiciona suporte para a interface [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) além do suporte à interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) fornecido pelo [**CBasePin**](cbasepin.md).

Para usar essa classe, derive uma nova classe e substitua pelo menos os seguintes métodos:

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin::Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Dependendo da função do pino, talvez seja necessário substituir métodos adicionais no `CBaseInputPin` ou **no CBasePin.**



| Variáveis de membro protegidas                                                 | Descrição                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | Ponteiro para o alocador de memória.                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | Sinalizador que indica se o alocador produz amostras de mídia somente leitura.                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | Sinalizador que indica se o pino está sendo liberado no momento.                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | Propriedades do exemplo mais recente.                                                                       |
| Métodos públicos                                                             | Descrição                                                                                                 |
| [**Cbaseinputpin**](cbaseinputpin-cbaseinputpin.md)                       | Método do construtor.                                                                                         |
| [**~CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Método destruidor.                                                                                          |
| [**Breakconnect**](cbaseinputpin-breakconnect.md)                         | Libera o pino de uma conexão.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Consulta se o alocador usa exemplos de mídia somente leitura.                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | Consulta se o filtro está sendo liberado no momento.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Determina se o pin pode aceitar exemplos. Virtual.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Passa uma mensagem de controle de qualidade para o objeto apropriado.                                                 |
| [**Inativo**](cbaseinputpin-inactive.md)                                 | Notifica o pino de que o filtro não está mais ativo. Virtual.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Recupera as propriedades do exemplo mais recente.                                                         |
| Métodos IPin                                                               | Descrição                                                                                                 |
| [**Beginflush**](cbaseinputpin-beginflush.md)                             | Inicia uma operação de liberação.                                                                                   |
| [**Endflush**](cbaseinputpin-endflush.md)                                 | Encerra uma operação de liberação.                                                                                     |
| Métodos IMemInputPin                                                       | Descrição                                                                                                 |
| [**Getallocator**](cbaseinputpin-getallocator.md)                         | Recupera o alocador de memória proposto por esse pino.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Especifica um alocador para a conexão.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Recupera as propriedades do alocador solicitadas pelo pino de entrada.                                              |
| [**Receber**](cbaseinputpin-receive.md)                                   | Recebe o próximo exemplo de mídia no fluxo.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Recebe vários exemplos no fluxo.                                                                    |
| [**Receivecanblock**](cbaseinputpin-receivecanblock.md)                   | Determina se as chamadas para o [**método CBaseInputPin::Receive**](cbaseinputpin-receive.md) podem ser bloqueados. |
| Métodos IQualityControl                                                    | Descrição                                                                                                 |
| [**Notificar**](cbaseinputpin-notify.md)                                     | Recebe uma mensagem de controle de qualidade.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




