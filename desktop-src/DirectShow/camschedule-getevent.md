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
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752312"
---
# <a name="camschedulegetevent-method"></a>Método CAMSchedule. GetEvent

O `GetEvent` método recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um identificador para um evento.

## <a name="remarks"></a>Comentários

Se a próxima hora do aviso for alterada em outras palavras, se uma nova solicitação de aviso for adicionada à frente da lista, o Agendador sinalizará esse evento. O relógio deve chamar o método [**CAMSchedule:: Advise**](camschedule-advise.md) para determinar o próximo horário de aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




