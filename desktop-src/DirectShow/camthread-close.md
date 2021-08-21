---
description: O método Close aguarda a saída do thread e libera seus recursos.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Método CAMThread.Close (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf12a80cd967832755f476db0e8810867326e84598ddce835e1da10dc6943419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158927"
---
# <a name="camthreadclose-method"></a>Método CAMThread.Close

O `Close` método aguarda a saída do thread e libera seus recursos.

## <a name="syntax"></a>Sintaxe


```C++
void Close();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve fornecer uma maneira de o thread sair. Por exemplo, no [**método CAMThread::ThreadProc,**](camthread-threadproc.md) defina uma solicitação que sinaliza o thread para sair. Em seguida, [**chame o método CAMThread::CallWorker**](camthread-callworker.md) com esse valor.

O [**método destruidor ~ CAMThread**](camthread--camthread.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




