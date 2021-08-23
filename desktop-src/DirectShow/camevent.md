---
description: A classe CAMEvent é um wrapper para eventos de redefinição manual e redefinição automática.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Classe CAMEvent (Wxutil.h)
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
ms.openlocfilehash: ea87239628f001feaa82f84ca8c50941b56d3eb99f486934b551e832d1f588c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955525"
---
# <a name="camevent-class"></a>Classe CAMEvent

![hierarquia de classes camevent](images/util06.png)

A **classe CAMEvent** é um wrapper para eventos de redefinição manual e redefinição automática.

Essa classe fornece uma maneira conveniente de gerenciar eventos, em vez de chamar funções como [**CreateEvent,**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)e [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variáveis de membro protegidas                          | Descrição                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | Alça de evento.                                                   |
| Métodos públicos                                      | Descrição                                                     |
| [**Camevent**](camevent-camevent.md)               | Método do construtor.                                             |
| [**~CAMEvent**](camevent--camevent.md)             | Método destruidor.                                              |
| [**Verificar**](camevent-check.md)                     | Verifica se o evento está definido, sem bloqueio.              |
| [**Redefinir**](camevent-reset.md)                     | Define o estado do evento como não sinal.                     |
| [**Definir**](camevent-set.md)                         | Sinaliza o evento.                                              |
| [**Aguarde**](camevent-wait.md)                       | Bloqueia até que o evento seja sinalizado ou até que ocorra um tempo-out. |
| Operadores                                           | Descrição                                                     |
| [**operador HANDLE**](camevent-operator-handle.md) | Recupera o alça de evento.                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

