---
description: O método get FramesDrawn recupera a variável de membro \_ m cFramesDrawn, dando o número de quadros \_ desenhados desde o início do streaming.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: CBaseVideoRenderer.get_FramesDrawn método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65a7c698d129a3606f6ba75f856289ca2b4e15c438d3890eb0a97e4a198ee808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822579"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a>Método CBaseVideoRenderer.get \_ FramesDrawn

O `get_FramesDrawn` método recupera a **variável de membro m \_ cFramesDrawn,** dando o número de quadros desenhados desde o início do streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcFramesDrawn* 
</dt> <dd>

Ponteiro para o número de quadros desenhados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IQualProp::get \_ FramesDrawn.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




