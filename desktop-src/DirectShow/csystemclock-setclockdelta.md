---
description: 'O método SetClockDelta ajusta a hora do relógio. Esse método implementa o método IAMClockAdjust:: SetClockDelta.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Método CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751678"
---
# <a name="csystemclocksetclockdelta-method"></a>Método CSystemClock. SetClockDelta

O `SetClockDelta` método ajusta a hora do relógio. Esse método implementa o método [**IAMClockAdjust:: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtDelta* 
</dt> <dd>

Especifica o valor pelo qual ajustar o relógio, como um valor [**de \_ tempo de referência**](reference-time.md) . Um valor positivo move o relógio para a frente e um valor negativo move o relógio para trás.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método simplesmente chama [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).

Os valores de tempo retornados por [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) são monotônicos aumentando. Se você definir o relógio de volta, **getTime** continuará relatando o tempo antigo até que o relógio interno se ajuste.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| parâmetro<br/>  | <dl> <dt>Sysclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




