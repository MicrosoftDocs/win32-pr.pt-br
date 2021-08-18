---
description: O método GetRenderEvent recupera o evento que agenda a renderização.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Método CBaseRenderer.GetRenderEvent (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b4adc030e172a3d66d501e745ca9e3d1062fc1551bccb504fff36328d00bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822653"
---
# <a name="cbaserenderergetrenderevent-method"></a>Método CBaseRenderer.GetRenderEvent

O `GetRenderEvent` método recupera o evento que agenda a renderização.

## <a name="syntax"></a>Sintaxe


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o [**evento CBaseRenderer::m \_ RenderEvent.**](cbaserenderer-m-renderevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




