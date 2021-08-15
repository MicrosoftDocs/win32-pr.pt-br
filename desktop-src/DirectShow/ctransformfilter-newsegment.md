---
description: O método NewSegment notifica o filtro de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Método CTransformFilter. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2cb83c376b012ae3474f87b0f8d26c7fb5560812c1d8ddcbb3ea62293797bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953545"
---
# <a name="ctransformfilternewsegment-method"></a>Método CTransformFilter. NewSegment

O `NewSegment` método notifica o filtro de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tStart* 
</dt> <dd>

Hora de início do segmento, em relação à fonte original.

</dd> <dt>

*tStop* 
</dt> <dd>

Hora de parada do segmento, em relação à fonte original.

</dd> <dt>

*dRate* 
</dt> <dd>

Taxa em que o segmento deve ser processado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O método [**CTransformInputPin:: NewSegment**](ctransforminputpin-newsegment.md) do pino de entrada chama esse método. Esse método entrega a `NewSegment` chamada para o pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




