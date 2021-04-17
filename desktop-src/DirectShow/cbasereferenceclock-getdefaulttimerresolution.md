---
description: O método GetDefaultTimerResolution retorna a resolução atual do temporizador do relógio de referência.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Método CBaseReferenceClock. GetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752510"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>Método CBaseReferenceClock. GetDefaultTimerResolution

O `GetDefaultTimerResolution` método retorna a resolução atual do temporizador do relógio de referência.

## <a name="syntax"></a>Sintaxe


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimerResolution* 
</dt> <dd>

Recebe a resolução do temporizador solicitada, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método implementa o método [**IReferenceClockTimerControl:: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




