---
description: O método ShouldDrawSampleNow determina se o vídeo deve ser desenhado sem configurar um link de aviso do temporizador com o relógio.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Método CBaseVideoRenderer.ShouldDrawSampleNow (Renbase.h)
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
ms.openlocfilehash: e3c0297ccf670de12380c5f02af2c67d6050bac29dd1fa7e7e89a6e6c7c20592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074680"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Método CBaseVideoRenderer.ShouldDrawSampleNow

O método determina se o vídeo deve ser desenhado sem `ShouldDrawSampleNow` definir um link de aviso do temporizador com o relógio.

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

Ponteiro para a hora de início da renderização.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Ponteiro para o tempo para parar a renderização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Retorna S OK para desenhar de uma vez sem esperar, S FALSE para significar desenhar no momento \_ \_ *ptrStart* ou um erro para significar que não desenhar o exemplo; ou seja, ignore-o para economizar tempo.

## <a name="remarks"></a>Comentários

Essa função membro substitui [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




