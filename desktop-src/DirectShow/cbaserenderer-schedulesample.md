---
description: O método ScheduleSample agenda um exemplo para renderização.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Método CBaseRenderer.ScheduleSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88e728b90078ab11a6215dad60a88b819b2c513071637e2aa5c6b6ed7226189b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157588"
---
# <a name="cbaserendererschedulesample-method"></a>Método CBaseRenderer.ScheduleSample

O `ScheduleSample` método agenda um exemplo para renderização.

## <a name="syntax"></a>Sintaxe


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample do**](/windows/desktop/api/Strmif/nn-strmif-imediasample) exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o exemplo tiver sido agendado ou **FALSE** se o exemplo tiver sido descartado.

## <a name="remarks"></a>Comentários

Esse método primeiro determina se o exemplo deve ser renderizado imediatamente, renderizado no futuro ou descartado. (Para fazer isso, ele chama o [**método CBaseRenderer::GetSampleTimes.)**](cbaserenderer-getsampletimes.md) Se o exemplo deve ser renderizado imediatamente, o método sinaliza o [**evento CBaseRenderer::m \_ RenderEvent.**](cbaserenderer-m-renderevent.md) Se o exemplo precisar ser renderizado no futuro, o método chamará o método [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para agendamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




