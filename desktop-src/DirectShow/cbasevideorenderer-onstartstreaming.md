---
description: O método OnStartStreaming redefine todas as vezes que controlam o streaming.
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: Método CBaseVideoRenderer.OnStartStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2a55d509c900c7be68d3225826c208755d31ef66e0c24119bd1d044dad1aefc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157051"
---
# <a name="cbasevideorendereronstartstreaming-method"></a>Método CBaseVideoRenderer.OnStartStreaming

O `OnStartStreaming` método redefine todas as vezes que controlam o streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro substitui [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




