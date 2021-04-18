---
description: O \_ método Get BitErrorRate recupera uma taxa aproximada de erros de bits para o vídeo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Método de CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
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
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755794"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>CBaseControlVideo. obter \_ método BitErrorRate

O `get_BitErrorRate` método recupera uma taxa aproximada de erros de bits para o vídeo.

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

Ponteiro para a taxa de erros de bits (um erro para aproximadamente este número de bits).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IBasicVideo:: get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) . Ele chama o método puro virtual [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




