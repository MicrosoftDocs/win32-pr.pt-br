---
description: Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: Membro CTransformFilter::m_bEOSDelivered (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38d27fabb9dd3ed2a37ed5d836bfdfb1036f4255e6af48580ab6e0678abad74b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655100"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Membro CTransformFilter::m \_ bEOSDelivered

Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Comentários

Se o filtro pausar quando não tiver uma conexão de entrada, ele enviará uma notificação de fim de fluxo downstream e define esse sinalizador como **TRUE.** A notificação de fim de fluxo garante que o filtro downstream não aguarde amostras. Observe que o método [**EndOfStream do**](ctransformfilter-endofstream.md) filtro não configura esse sinalizador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




