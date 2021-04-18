---
description: O método SignalTimerFired limpa o identificador do temporizador usado para agendar a renderização.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Método CBaseRenderer. SignalTimerFired (Renbase. h)
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
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757038"
---
# <a name="cbaserenderersignaltimerfired-method"></a>Método CBaseRenderer. SignalTimerFired

O `SignalTimerFired` método limpa o identificador do temporizador usado para agendar a renderização.

## <a name="syntax"></a>Sintaxe


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro chama esse método quando o temporizador de renderização é ativado (consulte [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) ou quando o temporizador é cancelado (consulte [**CBaseRenderer:: CancelNotification**](cbaserenderer-cancelnotification.md)). O método redefine a variável de membro [**CBaseRenderer:: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) para zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




