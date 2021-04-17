---
description: O método remove remove o item na posição especificada.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Método CGenericList. Remove (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752700"
---
# <a name="cgenericlistremove-method"></a>Método CGenericList. Remove

O `Remove` método remove o item na posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor de posição indicando o item a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo).

## <a name="remarks"></a>Comentários

Esse método exclui o nó da lista, mas não exclui o item contido nesse nó.

Se o *PDV* for **nulo**, o método retornará **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




