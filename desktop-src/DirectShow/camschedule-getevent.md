---
description: O método GetEvent recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Método CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e5126fde495c9553975daaf2db9e82de4ab4530a4629d217eba51818e20d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689076"
---
# <a name="camschedulegetevent-method"></a>Método CAMSchedule. GetEvent

O `GetEvent` método recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um identificador para um evento.

## <a name="remarks"></a>Comentários

Se a próxima hora do aviso for alterada em outras palavras, se uma nova solicitação de aviso for adicionada à frente da lista, o Agendador sinalizará esse evento. O relógio deve chamar o método [**CAMSchedule:: Advise**](camschedule-advise.md) para determinar o próximo horário de aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir Fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




