---
description: O método findi recupera a primeira posição que contém o item especificado.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Método CBaseList. findi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8bdd89de7e28c5645cf8a418a8472d484f891a499f11e238b80af5f7062ff4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635446"
---
# <a name="cbaselistfindi-method"></a>Método CBaseList. findi

O `FindI` método recupera a primeira posição que contém o item especificado.

## <a name="syntax"></a>Sintaxe


```C++
POSITION FindI(
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

Retorna um valor de posição ou **NULL** se o item não estiver na lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




