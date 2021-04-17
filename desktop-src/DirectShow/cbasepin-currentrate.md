---
description: 'O método CurrentRate recupera a taxa de segmento, definida pelo método CBasePin:: NewSegment.'
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Método CBasePin. CurrentRate (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747832"
---
# <a name="cbasepincurrentrate-method"></a>Método CBasePin. CurrentRate

O `CurrentRate` método recupera a taxa de segmento, definida pelo método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .

## <a name="syntax"></a>Sintaxe


```C++
double CurrentRate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o valor de [**CBasePin:: m \_ drate**](cbasepin-m-drate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




