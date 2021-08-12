---
description: O método \_ get AvgFrameRate calcula e recupera a taxa média de quadros obtida.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: CBaseVideoRenderer.get_AvgFrameRate método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79aab0677cfd5cba5f6a889519e0c12ed2236d8f82eca28b3fa7b227b941b2b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658779"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>Método CBaseVideoRenderer.get \_ AvgFrameRate

O `get_AvgFrameRate` método calcula e recupera a taxa média de quadros obtida.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

Ponteiro para o número de quadros por segundo desde o início do streaming.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IQualProp::get \_ AvgFrameRate.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




