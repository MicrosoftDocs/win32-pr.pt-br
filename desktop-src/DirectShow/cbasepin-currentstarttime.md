---
description: 'O método CurrentStartTime recupera a hora de início do segmento, definida pelo método CBasePin:: NewSegment.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Método CBasePin. CurrentStartTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c92355b397736b713fcf5fd09a61a130761a0cb954331b606ec1367fd65e6e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916736"
---
# <a name="cbasepincurrentstarttime-method"></a>Método CBasePin. CurrentStartTime

O `CurrentStartTime` método recupera a hora de início do segmento, definida pelo método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor de [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




