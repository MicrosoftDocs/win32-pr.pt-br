---
description: Recupera o próximo item da fila.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Método CQueue.GetQueueObject (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c32039a82e3a0b5c086cbe18e895bdec1aaac09d4947b90d9ba18e8c6636d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108276"
---
# <a name="cqueuegetqueueobject-method"></a>Método CQueue.GetQueueObject

Recupera o próximo item da fila.

## <a name="syntax"></a>Sintaxe


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um objeto do tipo **T** (o tipo de modelo).

## <a name="remarks"></a>Comentários

Esse método bloqueia até que um item seja disponibilizado na fila.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CQueue**](cqueue.md)
</dt> </dl>

 

 




