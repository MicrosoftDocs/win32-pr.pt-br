---
description: O método ResetEndOfStreamTimer cancela o temporizador que agenda as \_ notificações completas do EC.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Método CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e589288059eabbbbaaa23904ba021199cb051d9034345cb2c92ac946a6cba9c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502676"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a>Método CBaseRenderer. ResetEndOfStreamTimer

O `ResetEndOfStreamTimer` método cancela o temporizador que agenda as notificações [**\_ completas do EC**](ec-complete.md) .

## <a name="syntax"></a>Sintaxe


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> <dt>

[**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




