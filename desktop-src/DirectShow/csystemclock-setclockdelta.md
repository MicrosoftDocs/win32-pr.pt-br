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
ms.openlocfilehash: c98ccf35e41886594a3aab8c3abec6737128d8d7e22f6dfb75d0ac88ac3b7a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538656"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método simplesmente chama [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).

Os valores de tempo retornados por [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) são monotônicos aumentando. Se você definir o relógio de volta, **getTime** continuará relatando o tempo antigo até que o relógio interno se ajuste.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| Cabeçalho<br/>  | <dl> <dt>Sysclock. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




