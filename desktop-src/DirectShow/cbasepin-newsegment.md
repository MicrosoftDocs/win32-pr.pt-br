---
description: O método NewSegment notifica o pin de que os exemplos de mídia recebidos após essa chamada são agrupados como um segmento. Implementa o método IPin::NewSegment.
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Método CBasePin.NewSegment (Amfilter.h)
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
ms.openlocfilehash: ed3ffc9cc0656509b29a6c32baeaf7311437a79e8402fbae0727cf9f93a30abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384546"
---
# <a name="cbasepinnewsegment-method"></a>Método CBasePin.NewSegment

O `NewSegment` método notifica o pin de que os exemplos de mídia recebidos após essa chamada são agrupados como um segmento. Implementa o [**método IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

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

*Tstart* 
</dt> <dd>

Posição de mídia inicial do segmento, em unidades de 100 nanossegundos.

</dd> <dt>

*tStop* 
</dt> <dd>

Posição de mídia final do segmento, em unidades de 100 nanossegundos.

</dd> <dt>

*dRate* 
</dt> <dd>

Taxa na qual esse segmento deve ser processado, como um percentual da taxa original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método define as variáveis de membro [**CBasePin::m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md)e [**CBasePin::m \_ dRate.**](cbasepin-m-drate.md) Na classe derivada, substitua esse método para passar a notificação downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




