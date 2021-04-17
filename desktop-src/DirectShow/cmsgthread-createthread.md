---
description: Cria um thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Método CMsgThread. CreateThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749248"
---
# <a name="cmsgthreadcreatethread-method"></a>Método CMsgThread. CreateThread

Cria um thread.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                              | Descrição                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>VERDADEIRO * * * *</dt> </dl>  | O thread foi criado com êxito.<br/>     |
| <dl> <dt>FALSE * * * *</dt> </dl> | O thread não foi criado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

O thread fará um loop, bloqueando até que uma solicitação seja enfileirada (por meio da função de membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e, em seguida, chamando a função de membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) com cada mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




