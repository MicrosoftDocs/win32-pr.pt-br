---
description: 'O método NewSegment notifica o PIN de que amostras de mídia recebidas após essa chamada são agrupadas como um segmento. Esse método implementa o método IPin:: NewSegment.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Método CTransformInputPin. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759087"
---
# <a name="ctransforminputpinnewsegment-method"></a>Método CTransformInputPin. NewSegment

O `NewSegment` método notifica o PIN de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento. Esse método implementa o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tStart* 
</dt> <dd>

Hora de início do segmento.

</dd> <dt>

*tStop* 
</dt> <dd>

Hora de parada do segmento.

</dd> <dt>

*dRate* 
</dt> <dd>

Taxa do segmento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) . Ele chama o método [**CTransformFilter:: NewSegment**](ctransformfilter-newsegment.md) do filtro para entregar a chamada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




