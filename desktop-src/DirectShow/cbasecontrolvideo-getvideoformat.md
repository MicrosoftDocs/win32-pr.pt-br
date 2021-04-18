---
description: O método GetVideoFormat recupera um exemplo de vídeo que representa o formato de vídeo atual.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Método CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754772"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>Método CBaseControlVideo. GetVideoFormat

O `GetVideoFormat` método recupera um exemplo de vídeo que representa o formato de vídeo atual.

## <a name="syntax"></a>Sintaxe


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém o formato de vídeo atual.

## <a name="remarks"></a>Comentários

Para retornar e verificar determinadas informações por meio de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), o objeto deve saber o formato de vídeo atual. Ele obtém essas informações chamando esse método virtual puro que as classes derivadas devem substituir. Essa função de membro é chamada pelas seguintes funções de membro [**CBaseControlVideo**](cbasecontrolvideo.md) .

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo:: obter \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo:: obter \_ taxa de bits**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo:: obter \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo:: obter \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo:: obter \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




