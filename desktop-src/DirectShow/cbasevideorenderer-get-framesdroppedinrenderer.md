---
description: O método \_ get FramesDroppedInRenderer recupera o número de quadros descartados pelo renderista.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: CBaseVideoRenderer.get_FramesDroppedInRenderer método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21bd2e9c2f9edb50ca3800c95b59ba19fd91674d5ef343cf35842380ce617978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016754"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>Método CBaseVideoRenderer.get \_ FramesDroppedInRenderer

O `get_FramesDroppedInRenderer` método recupera o número de quadros descartados pelo renderista.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcFramesDropped* 
</dt> <dd>

Ponteiro para o número de quadros descartados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IQualProp::get \_ FramesDroppedInRenderer.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) É assim que a página de propriedades recupera os dados do agendador. Os quadros também podem ser descartados upstream sem que o renderador os veja.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




