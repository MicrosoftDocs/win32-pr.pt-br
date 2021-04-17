---
description: O método GetNext recupera o item na posição especificada e avança a posição.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Método CGenericList. GetNext (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749249"
---
# <a name="cgenericlistgetnext-method"></a>Método CGenericList. GetNext

O `GetNext` método recupera o item na posição especificada e avança a posição.

## <a name="syntax"></a>Sintaxe


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RP* \[ referência\]
</dt> <dd>

Referência a um valor de posição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo).

## <a name="remarks"></a>Comentários

Esse método avança o indicador de posição para a próxima posição. Se o indicador de posição passar do final da lista, o método o definirá como **nulo**.

Se o *RP* for **nulo**, o método retornará **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




