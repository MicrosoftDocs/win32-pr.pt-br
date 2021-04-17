---
description: O método SetTimeDelta ajusta a hora interna do relógio.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Método CBaseReferenceClock. SetTimeDelta (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811750"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Método CBaseReferenceClock. SetTimeDelta

O `SetTimeDelta` método ajusta a hora interna do relógio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Timedelta* \[ referência\]
</dt> <dd>

Valor para ajustar a hora do relógio, em unidades de 100 a nanossegundos. Um valor positivo move o relógio para a frente e um valor negativo move o relógio para trás.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

A classe derivada pode usar esse método para ajustar o relógio interno, caso ele se descompasso do dispositivo que está fornecendo informações de tempo.

O método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) nunca retorna valores decrescentes. Se você ajustar o relógio para trás, **getTime** retornará o valor anterior até que o relógio atinja esse valor novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




