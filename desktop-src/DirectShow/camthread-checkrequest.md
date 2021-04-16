---
description: O método CheckRequest verifica se há uma solicitação, sem bloqueio.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Método CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779859"
---
# <a name="camthreadcheckrequest-method"></a>Método CAMThread. CheckRequest

O `CheckRequest` método verifica se há uma solicitação, sem bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pParam* 
</dt> <dd>

Ponteiro para uma variável que recebe o valor passado na última chamada para o método [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se houver uma solicitação pendente ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método é uma versão sem bloqueio do método [**CAMThread:: GetRequest**](camthread-getrequest.md) .

Se outro thread estiver aguardando uma chamada para CallWorker, esse método recuperará o parâmetro de solicitação e retornará **true**. Caso contrário, retornará **false**. Se o método retornar **true**, chame o método [**CAMThread:: Reply**](camthread-reply.md) para liberar o thread solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




