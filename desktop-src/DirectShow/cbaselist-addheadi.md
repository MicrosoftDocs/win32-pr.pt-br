---
description: O método AddHeadI adiciona um item à frente da lista.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Método CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754566"
---
# <a name="cbaselistaddheadi-method"></a>Método CBaseList. AddHeadI

O `AddHeadI` método adiciona um item à frente da lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObj* 
</dt> <dd>

Ponteiro para o item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de posição que indica a nova posição de cabeçalho.

## <a name="remarks"></a>Comentários

Se o método falhar, o valor de retorno será **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




