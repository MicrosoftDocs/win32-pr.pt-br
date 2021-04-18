---
description: O \_ método Get VideoWidth recupera a largura do vídeo nativo.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Método de CBaseControlVideo.get_VideoWidth (Ctlutil. h)
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
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749050"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>CBaseControlVideo. obter \_ método VideoWidth

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

## <a name="return-value"></a>Retornar valor

Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IBasicVideo:: get \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) . Ele chama o CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




