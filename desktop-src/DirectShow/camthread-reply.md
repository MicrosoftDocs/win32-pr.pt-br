---
description: O método Reply responde a uma solicitação.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Método CAMThread.Reply (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9783703d711800b8002aa0372292349d83620eafb097be2256ffde6ab2c91c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662362"
---
# <a name="camthreadreply-method"></a>Método CAMThread.Reply

O `Reply` método responde a uma solicitação.

## <a name="syntax"></a>Sintaxe


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dw* 
</dt> <dd>

Valor a ser retornada [**no método CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método CallWorker bloqueia até que esse método seja chamado. O *parâmetro dw* fornece o valor de retorno para CallWorker. Chame esse método em seu procedimento de thread depois de recuperar uma solicitação para liberar o thread solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




