---
description: O método SetTimeDelta ajusta a hora do relógio interna.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Método CBaseReferenceClock.SetTimeDelta (Refclock.h)
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
ms.openlocfilehash: ac9eba5337fa43e43e3b7a45a7a92263fd4e6d69388185a2096c1a270590e482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403435"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Método CBaseReferenceClock.SetTimeDelta

O `SetTimeDelta` método ajusta a hora do relógio interna.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TimeDelta* \[ Ref\]
</dt> <dd>

Valor para ajustar a hora do relógio, em unidades de 100 nanossegundos. Um valor positivo move o relógio para frente e um valor negativo move o relógio para trás.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

A classe derivada pode usar esse método para ajustar o relógio interno, se ele se desgarrapar do dispositivo que está fornecendo informações de tempo.

O [**método CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) nunca retorna valores decrescentes. Se você ajustar o relógio para trás, **GetTime** retornará o valor anterior até que o relógio atinja esse valor novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




