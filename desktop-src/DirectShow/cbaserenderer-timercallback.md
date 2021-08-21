---
description: O método TimerCallback é um método de retorno de chamada para o evento de temporizador de fim de fluxo.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Método CBaseRenderer.TimerCallback (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d3164959ecaa701397b5550c43449884208df1110300b6a042879ac4f146584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537426"
---
# <a name="cbaserenderertimercallback-method"></a>Método CBaseRenderer.TimerCallback

O método é um método de retorno de chamada para o evento de temporizador de fim `TimerCallback` de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O [**método CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) usa um evento de temporizador para agendar notificações EC \_ COMPLETE. O **método CBaseRenderer::TimerCallback** é a função de retorno de chamada para o evento de temporizador. O `TimerCallback` método chama **SendEndOfStream** novamente e **SendEndOfStream** determina se deve enviar a notificação EC \_ COMPLETE ou definir outro temporizador.

O [**método CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) cancela o evento de temporizador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




