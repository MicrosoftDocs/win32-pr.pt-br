---
description: O método GetRequest aguarda a próxima solicitação.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Método CAMThread. GetRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760287"
---
# <a name="camthreadgetrequest-method"></a>Método CAMThread. GetRequest

O `GetRequest` método aguarda a próxima solicitação.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor que é definido pela classe derivada.

## <a name="remarks"></a>Comentários

Esse método é bloqueado até que outro thread chame o método [**CAMThread:: CallWorker**](camthread-callworker.md) . Em seguida, ele retorna o parâmetro que foi passado para CallWorker. Chame o método [**CAMThread:: Reply**](camthread-reply.md) para liberar o thread solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




