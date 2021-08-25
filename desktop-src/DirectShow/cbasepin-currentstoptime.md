---
description: O método CurrentStopTime recupera o tempo de parada do segmento, definido pelo método CBasePin::NewSegment.
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Método CBasePin.CurrentStopTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2905913828c91fffde9fb474802c8dea0e0f83d59ccdb5408f846a1936071cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916696"
---
# <a name="cbasepincurrentstoptime-method"></a>Método CBasePin.CurrentStopTime

O `CurrentStopTime` método recupera a hora de parada do segmento, definida pelo método [**CBasePin::NewSegment.**](cbasepin-newsegment.md)

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor de [**CBasePin::m \_ tStop.**](cbasepin-m-tstop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




