---
description: O método ScheduleSample agenda uma amostra para renderização.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Método CBaseRenderer. ScheduleSample (Renbase. h)
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
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748820"
---
# <a name="cbaserendererschedulesample-method"></a>Método CBaseRenderer. ScheduleSample

O `ScheduleSample` método agenda uma amostra para renderização.

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

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se o exemplo foi agendado ou **false** se o exemplo foi Descartado.

## <a name="remarks"></a>Comentários

Esse método primeiro determina se o exemplo deve ser renderizado imediatamente, renderizado no futuro ou descartado. (Para fazer isso, ele chama o método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) .) Se o exemplo deve ser processado imediatamente, o método sinaliza o evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) . Se o exemplo for renderizado no futuro, o método chamará o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para agendamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




