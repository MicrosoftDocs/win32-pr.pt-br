---
description: O método getpróximoi recupera o item na posição especificada e avança a posição.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Método CBaseList. GetNextI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758872"
---
# <a name="cbaselistgetnexti-method"></a>Método CBaseList. getavançari

O `GetNextI` método recupera o item na posição especificada e avança a posição.

## <a name="syntax"></a>Sintaxe


```C++
void* GetNextI(
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

Retorna um ponteiro para o item. Se o *RP* for **nulo**, o método retornará **NULL**.

## <a name="remarks"></a>Comentários

Esse método avança o indicador de posição para a próxima posição. Se o indicador de posição passar do final da lista, o método o definirá como **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




