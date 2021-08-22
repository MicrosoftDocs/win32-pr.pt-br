---
description: O método \_ get VideoWidth recupera a largura do vídeo nativo.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: CBaseControlVideo.get_VideoWidth método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268316dd9b7f37894f60ed45878c7de9bbc8d379301daa7bbefedcadd0b8e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661373"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>Método CBaseControlVideo.get \_ VideoWidth

O `get_VideoWidth` método recupera a largura do vídeo nativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoWidth* 
</dt> <dd>

Ponteiro para a largura do vídeo nativo, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IBasicVideo::get \_ VideoWidth.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) Ele chama o [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtual puro para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




