---
description: O método Get taxa de bits \_ recupera uma taxa aproximada do vídeo.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Método de CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b33e3584bb0460b798101d8062c3647b983841c77653adcffd18580eade25c6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057266"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>Método de taxa de bits CBaseControlVideo. get \_

O `get_BitRate` método recupera uma taxa de bits aproximada para o vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBitRate* 
</dt> <dd>

Ponteiro para a taxa de bits, em bits por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna NOERROR se for successful ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IBasicVideo:: get \_ taxa de bits**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) . Ele chama o CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




