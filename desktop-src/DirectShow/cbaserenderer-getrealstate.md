---
description: O método GetRealState recupera o estado do filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Método CBaseRenderer.GetRealState (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c65ac4310abddc619296776981040cc5e1e6c5ad48ce37ea24210bc5a85d94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403415"
---
# <a name="cbaserenderergetrealstate-method"></a>Método CBaseRenderer.GetRealState

O `GetRealState` método recupera o estado do filtro.

## <a name="syntax"></a>Sintaxe


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor de [**CBaseFilter::m \_ State**](cbasefilter-m-state.md). O valor é um membro do tipo [**enumerado FILTER \_ STATE.**](/windows/win32/api/strmif/ne-strmif-filter_state)

## <a name="remarks"></a>Comentários

Esse método fornece uma alternativa mais simples ao [**método CBaseRenderer::GetState,**](cbaserenderer-getstate.md) para uso interno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




