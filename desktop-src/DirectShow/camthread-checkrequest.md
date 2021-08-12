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
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662351"
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

## <a name="return-value"></a>Valor retornado

Retorna **true** se houver uma solicitação pendente ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método é uma versão sem bloqueio do método [**CAMThread:: GetRequest**](camthread-getrequest.md) .

Se outro thread estiver aguardando uma chamada para CallWorker, esse método recuperará o parâmetro de solicitação e retornará **true**. Caso contrário, retornará **false**. Se o método retornar **true**, chame o método [**CAMThread:: Reply**](camthread-reply.md) para liberar o thread solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




