---
description: O método OnStartStreaming é chamado quando o filtro começa a transmitir.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Método CBaseRenderer.OnStartStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b0f050222b0ca6a88c7cf1d9348597e4d7b68f2a2ed431b4f6843afe97efd5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157669"
---
# <a name="cbaserendereronstartstreaming-method"></a>Método CBaseRenderer.OnStartStreaming

O `OnStartStreaming` método é chamado quando o filtro começa a transmitir.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O [**método CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) chama esse método. Ele não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




