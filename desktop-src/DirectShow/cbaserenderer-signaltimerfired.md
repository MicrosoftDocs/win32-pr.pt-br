---
description: O método SignalTimerFired limpa o identificador de temporizador usado para agendar a renderização.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Método CBaseRenderer.SignalTimerFired (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f08ed0e8348648d5d1af1127159b414b0ddbc40cfd470ff0834b7bc2b0723e9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052356"
---
# <a name="cbaserenderersignaltimerfired-method"></a>Método CBaseRenderer.SignalTimerFired

O `SignalTimerFired` método limpa o identificador de temporizador usado para agendar a renderização.

## <a name="syntax"></a>Sintaxe


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro chama esse método quando o temporizador de renderização é ativado (consulte [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) ou quando o temporizador é cancelado (consulte [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)). O método redefine a variável de [**membro CBaseRenderer::m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) para zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




