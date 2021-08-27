---
description: O método CallWorker sinaliza o thread com uma solicitação.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Método CAMThread. CallWorker (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7ffee6a55191f8f41d7121f3801a4a6392f9869803ded40ed891817146828f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955395"
---
# <a name="camthreadcallworker-method"></a>Método CAMThread. CallWorker

O `CallWorker` método sinaliza o thread com uma solicitação.

## <a name="syntax"></a>Sintaxe


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* 
</dt> <dd>

Parâmetro de solicitação. A classe derivada define o significado do parâmetro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor que é definido pela classe derivada.

## <a name="remarks"></a>Comentários

Os métodos [**CAMThread:: GetRequest**](camthread-getrequest.md) e [**CAMThread:: CheckRequest**](camthread-checkrequest.md) recuperam o valor do parâmetro *dwParam* . O método GetRequest é bloqueado até que `CallWorker` seja chamado.

Esse método é bloqueado até que o método [**CAMThread:: Reply**](camthread-reply.md) seja chamado. O valor de retorno é o parâmetro fornecido para reply.

Esse método contém o bloqueio [**CAMThread:: m \_ AccessLock**](camthread-m-accesslock.md) para serializar solicitações. Portanto, chame esse método do próprio thread ou de qualquer função de membro que seja executada no contexto do thread.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




