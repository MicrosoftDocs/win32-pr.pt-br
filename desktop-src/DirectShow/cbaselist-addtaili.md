---
description: O método AddTailI adiciona um item ao final da lista.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Método CBaseList.AddTailI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659122"
---
# <a name="cbaselistaddtaili-method"></a>Método CBaseList.AddTailI

O `AddTailI` método adiciona um item ao final da lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObj* 
</dt> <dd>

Ponteiro para o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor POSITION para a nova posição da parte final.

## <a name="remarks"></a>Comentários

Se o método falhar, ele retornará **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




