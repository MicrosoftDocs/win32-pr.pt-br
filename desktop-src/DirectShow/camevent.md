---
description: A classe CAMEvent é um wrapper para eventos de redefinição manual e redefinição automática.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Classe CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750715"
---
# <a name="camevent-class"></a>Classe CAMEvent

![hierarquia de classe CAMEvent](images/util06.png)

A classe **CAMEvent** é um wrapper para eventos de redefinição manual e redefinição automática.

Essa classe fornece uma maneira conveniente de gerenciar eventos, em vez de chamar funções como, por exemplo, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)e [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variáveis de membro protegido                          | Descrição                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**\_hEvent m**](camevent-m-hevent.md)              | Identificador de evento.                                                   |
| Métodos públicos                                      | Descrição                                                     |
| [**CAMEvent**](camevent-camevent.md)               | Método de construtor.                                             |
| [**~ CAMEvent**](camevent--camevent.md)             | Método destruidor.                                              |
| [**Verificação**](camevent-check.md)                     | Verifica se o evento está definido, sem bloqueio.              |
| [**Redefinir**](camevent-reset.md)                     | Define o estado do evento como não sinalizado.                     |
| [**Definir**](camevent-set.md)                         | Sinaliza o evento.                                              |
| [**Aguarde**](camevent-wait.md)                       | Bloqueia até que o evento seja sinalizado ou até que ocorra um tempo limite. |
| Operadores                                           | Descrição                                                     |
| [**IDENTIFICADOR do operador**](camevent-operator-handle.md) | Recupera o identificador de evento.                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

