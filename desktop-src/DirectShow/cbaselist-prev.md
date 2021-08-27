---
description: O método anterior recupera a posição anterior na lista.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Método CBaseList. anterior (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d04a63079e401b89286e10e927b540f40d04fc186546dbdbd4e31e8610fe617d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076596"
---
# <a name="cbaselistprev-method"></a>Método CBaseList. anterior

O `Prev` método recupera a posição anterior na lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor da posição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o indicador de posição anterior à posição especificada no *PDV*.

## <a name="remarks"></a>Comentários

Se *pos* for a primeira posição na lista, o método retornará **NULL**. Se o *PDV* for **nulo**, o método retornará a última posição na lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




