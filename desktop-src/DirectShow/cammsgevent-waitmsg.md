---
description: O método WaitMsg aguarda o evento ser sinalizado, enquanto envia mensagens enviadas.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Método CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a2169d9938a8c2ff8a1961eee0895fefd7cc8a2dd487a4193d8053d27d98ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955445"
---
# <a name="cammsgeventwaitmsg-method"></a>Método CAMMsgEvent. WaitMsg

O `WaitMsg` método aguarda que o evento seja sinalizado, enquanto envia mensagens enviadas.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwTimeOut* 
</dt> <dd>

Valor de tempo limite opcional, em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se o evento for sinalizado ou **false** se o tempo limite tiver ocorrido.

## <a name="remarks"></a>Comentários

Esse método chama a função PeekMessage para processar mensagens. Chame esse método em vez de [**CAMEvent:: Wait**](camevent-wait.md) se seu thread precisar processar mensagens enquanto aguarda um evento. Se o thread não processar mensagens e outro thread enviar uma mensagem, o deadlock poderá ocorrer.

Por exemplo, suponha que você crie um thread e, em seguida, bloqueie até que o thread seja inicializado. Se o thread enviar uma mensagem à sua janela chamando a função SendMessage, isso resultará em um deadlock. Isso ocorre porque SendMessage não retorna até que a mensagem seja processada. Chamar WaitMsg permite que a chamada SendMessage seja retornada, impedindo o deadlock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




