---
description: O método GetDueHandle recupera o identificador de evento a ser sinalizado.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Método CCmdQueue. GetDueHandle (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778507"
---
# <a name="ccmdqueuegetduehandle-method"></a>Método CCmdQueue. GetDueHandle

O `GetDueHandle` método recupera o identificador de evento a ser sinalizado.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o identificador de evento.

## <a name="remarks"></a>Comentários

Retornar o identificador de evento sempre que houver comandos adiados que são devidos à execução (quando [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md) não será bloqueado).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




