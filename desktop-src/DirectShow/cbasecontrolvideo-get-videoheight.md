---
description: O método \_ get VideoHeight recupera a altura do vídeo nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: CBaseControlVideo.get_VideoHeight método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057076"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>Método CBaseControlVideo.get \_ VideoHeight

O `get_VideoHeight` método recupera a altura do vídeo nativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoHeight* 
</dt> <dd>

Ponteiro para a altura do vídeo nativo, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IBasicVideo::get \_ VideoHeight.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) Ele chama o [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtual puro para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




