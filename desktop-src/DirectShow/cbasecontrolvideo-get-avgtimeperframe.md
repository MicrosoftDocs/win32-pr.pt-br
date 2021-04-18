---
description: O \_ método Get AvgTimePerFrame recupera o tempo médio por quadro.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Método de CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785500"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>CBaseControlVideo. obter \_ método AvgTimePerFrame

O `get_AvgTimePerFrame` método recupera o tempo médio por quadro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAvgTimePerFrame* 
</dt> <dd>

Ponteiro para o tempo médio por quadro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IBasicVideo:: get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) . Ele chama a função de membro puramente virtual [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




