---
description: O método AddAfterI insere um item após a posição especificada.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Método CBaseList. addifi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750707"
---
# <a name="cbaselistaddafteri-method"></a>Método CBaseList. addifi

O `AddAfterI` método insere um item após a posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Posição após a qual adicionar o item.

</dd> <dt>

*pObj* 
</dt> <dd>

Ponteiro para o item a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o indicador de posição do item inserido.

## <a name="remarks"></a>Comentários

Se o *PDV* for **nulo**, esse método adicionará o item ao cabeçalho da lista (equivalente a chamar o método [**CBaseList:: AddHeadI**](cbaselist-addheadi.md) ).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




