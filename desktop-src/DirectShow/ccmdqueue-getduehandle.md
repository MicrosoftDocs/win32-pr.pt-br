---
description: O método GetDueHandle recupera o alça de evento a ser sinalizado.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Método CCmdQueue.GetDueHandle (Winutil.h)
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
ms.openlocfilehash: 62fbe0e38e24891add93e63e0c03d521289ed345078e8e567a376e9bd639d997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016414"
---
# <a name="ccmdqueuegetduehandle-method"></a>Método CCmdQueue.GetDueHandle

O `GetDueHandle` método recupera o alça de evento a ser sinalizado.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o alça de evento.

## <a name="remarks"></a>Comentários

Retorne o alçamento de evento sempre que houver comandos adiados que devem ser executados (quando [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) não for bloqueado).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




