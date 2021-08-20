---
description: O método IsUsingDefaultDestination determina se o renderizador está usando a janela de destino padrão.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Método CBaseControlVideo. IsUsingDefaultDestination (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf254ec89cc6804af86c98abaaa0c53ae5f76a25766391529ca4de85bee7d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955215"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a>Método CBaseControlVideo. IsUsingDefaultDestination

O `IsUsingDefaultDestination` método determina se o renderizador está usando a janela de destino padrão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se estiver usando o destino padrão; caso contrário, retornará S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




