---
description: O método ShouldDrawSampleNow determina se o vídeo deve ser desenhado sem definir um link de aviso de temporizador com o relógio.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Método CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758553"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Método CBaseVideoRenderer. ShouldDrawSampleNow

O `ShouldDrawSampleNow` método determina se o vídeo deve ser desenhado sem definir um link de aviso de temporizador com o relógio.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) para o exemplo.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Ponteiro para o tempo para começar a renderização.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Ponteiro para a hora para parar a renderização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Retorna S \_ OK para a média desenhar ao mesmo tempo sem espera, S \_ false para significar Draw no time *ptrStart* ou um erro para significar não desenhar o exemplo; ou seja, ignorá-lo para economizar tempo.

## <a name="remarks"></a>Comentários

Essa função de membro substitui [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




