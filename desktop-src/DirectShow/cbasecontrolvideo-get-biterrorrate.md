---
description: O método \_ get BitErrorRate recupera uma taxa de erro de bit aproximada para o vídeo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: CBaseControlVideo.get_BitErrorRate método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057286"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Método CBaseControlVideo.get \_ BitErrorRate

O `get_BitErrorRate` método recupera uma taxa de erro de bit aproximada para o vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBitErrorRate* 
</dt> <dd>

Ponteiro para a taxa de erro de bit (um erro para aproximadamente esses muitos bits).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IBasicVideo::get \_ BitErrorRate.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) Ele chama o método [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtual puro para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




