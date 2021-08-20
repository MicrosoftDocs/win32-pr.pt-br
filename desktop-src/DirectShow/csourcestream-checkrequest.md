---
description: O método CheckRequest verifica se há uma solicitação de thread, sem bloqueio.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Método CSourceStream.CheckRequest (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bb77358ec579415439c2832b00255e7ffeb3c7eba0e387bfa0522a4a5109669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073310"
---
# <a name="csourcestreamcheckrequest-method"></a>Método CSourceStream.CheckRequest

O `CheckRequest` método verifica se há uma solicitação de thread, sem bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pcom* 
</dt> <dd>

Ponteiro para uma variável que recebe o valor passado na última chamada para o [**método CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se houver uma solicitação pendente ou **FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CAMThread::CheckRequest**](camthread-checkrequest.md) para executar a verificação de tipo. A **classe CSourceStream** define o seguinte tipo enumerado para o *parâmetro pCom:*


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




