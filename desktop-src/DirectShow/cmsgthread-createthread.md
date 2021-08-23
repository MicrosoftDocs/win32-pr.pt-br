---
description: Cria um thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Método CMsgThread.CreateThread (Msgthrd.h)
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
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831866"
---
# <a name="cmsgthreadcreatethread-method"></a>Método CMsgThread.CreateThread

Cria um thread.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                              | Descrição                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>TRUE****</dt> </dl>  | O thread foi criado com êxito.<br/>     |
| <dl> <dt>FALSE****</dt> </dl> | O thread não foi criado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

O thread fará um loop, bloqueando até que uma solicitação seja enxuta (por meio da função membro [**CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) e, em seguida, chamando a função de membro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) com cada mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




