---
description: 'O método GetRequestHandle recupera um identificador para o evento que é sinalizado pelo método CAMThread:: CallWorker.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Método CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fa1be333ff35821f187cea980746c6b729a05c12e2103f4465bb44bbcc6f9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652586"
---
# <a name="camthreadgetrequesthandle-method"></a>Método CAMThread. GetRequestHandle

O `GetRequestHandle` método recupera um identificador para o evento que é sinalizado pelo método [**CAMThread:: CallWorker**](camthread-callworker.md) .

## <a name="syntax"></a>Sintaxe


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um identificador de evento.

## <a name="remarks"></a>Comentários

A classe CAMEvent mantém um evento particular de redefinição manual, que é definido por CallWorker e redefinido pelo método [**CAMThread:: Reply**](camthread-reply.md) .

Se você chamar uma função como WaitForMultipleObjects, use GetRequestHandle para recuperar o identificador de evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




