---
description: O método TimerCallback é um método de retorno de chamada para o evento de timer de fim de fluxo.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Método CBaseRenderer. TimerCallback (Renbase. h)
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
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749627"
---
# <a name="cbaserenderertimercallback-method"></a>Método CBaseRenderer. TimerCallback

O `TimerCallback` método é um método de retorno de chamada para o evento de timer de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) usa um evento de timer para agendar \_ notificações completas do EC. O método **CBaseRenderer:: TimerCallback** é a função de retorno de chamada para o evento timer. O `TimerCallback` método chama **SendEndOfStream** novamente e **SendEndOfStream** determina se a notificação completa do EC deve ser enviada \_ ou definida outro temporizador.

O método [**CBaseRenderer:: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) cancela o evento timer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




