---
description: Retornará FALSE se o thread atual for o proprietário da seção crítica especificada.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Função CritCheckOut (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787394"
---
# <a name="critcheckout-function"></a>Função CritCheckOut

Retornará **false** se o thread atual for o proprietário da seção crítica especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Ponteiro para uma seção crítica [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em compilações de depuração, retorna **falso** se o thread atual for o proprietário desta seção crítica ou **verdadeiro** caso contrário. Em compilações de varejo, sempre retorna **true**.

## <a name="remarks"></a>Comentários

Essa função é o inverso da função [**CritCheckIn**](critcheckin.md) . Se **CritCheckIn** retornar **true**, **CritCheckOut** retornará **false** e vice-versa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de depuração de seção crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




