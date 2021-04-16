---
description: 'O método NewSegment notifica o PIN de que amostras de mídia recebidas após essa chamada são agrupadas como um segmento. Implementa o método IPin:: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Método CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751263"
---
# <a name="cbasepinnewsegment-method"></a>Método CBasePin. NewSegment

O `NewSegment` método notifica o PIN de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento. Implementa o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

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

Iniciando a posição de mídia do segmento, em unidades de 100 a nanossegundos.

</dd> <dt>

*tStop* 
</dt> <dd>

Terminar a posição de mídia do segmento, em unidades de 100 a nanossegundos.

</dd> <dt>

*dRate* 
</dt> <dd>

Taxa na qual esse segmento deve ser processado, como uma porcentagem da taxa original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método define as variáveis de membro [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md)e [**CBasePin:: m \_ drate**](cbasepin-m-drate.md) . Na classe derivada, substitua esse método para passar o downstream de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




