---
description: O método addantesi insere um item antes da posição especificada.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Método CBaseList. addantesi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfb995e614904e807e67eeee9c0f344525fd701d039c596eb081b6ff3be4f078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823743"
---
# <a name="cbaselistaddbeforei-method"></a>Método CBaseList. addantesi

O `AddBeforeI` método insere um item antes da posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Posição antes da qual adicionar o item.

</dd> <dt>

*pObj* 
</dt> <dd>

Ponteiro para o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o indicador de posição do item inserido.

## <a name="remarks"></a>Comentários

Se o *PDV* for **nulo**, esse método adicionará o item à parte final da lista (equivalente a chamar o método [**CBaseList:: addcaudai**](cbaselist-addtaili.md) ).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




