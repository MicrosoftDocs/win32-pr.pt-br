---
description: O modelo de classe CQueue implementa uma fila simples e de tamanho estático.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Classe CQueue (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760753"
---
# <a name="cqueue-class"></a>Classe CQueue

O modelo de classe **CQueue** implementa uma fila simples e de tamanho estático.



| Métodos públicos                                  | Descrição                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Método de construtor.                     |
| [**~ CQueue**](cqueue--cqueue.md)               | Método destruidor.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Recupera o próximo item da fila. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Coloca um item na fila.            |



 

## <a name="remarks"></a>Comentários

O construtor de classe especifica o tamanho da fila. Use o [**CQueue::P utqueueobject**](cqueue-putqueueobject.md) para colocar um item na fila e o método [**CQueue:: GetQueueObject**](cqueue-getqueueobject.md) para retirar um item da fila. Se a fila estiver cheia, o método **PutQueueObject** será bloqueado até que um item seja removido da fila. Se a fila estiver vazia, os blocos **GetQueueObject** até que um item seja enfileirado. O parâmetro de modelo especifica o tipo de item. Por exemplo:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



A classe usa dois semáforos para controlar as operações de enfileiramento, um semáforo "Get" e um semáforo "Put". O método [**GetQueueObject**](cqueue-getqueueobject.md) aguarda o semáforo "Get" (usando a função **WaitForSingleObject** ) e libera o sinal "Put" (usando a função **ReleaseSemaphore** ). O método [**PutQueueObject**](cqueue-putqueueobject.md) aguarda o semáforo "Put" e libera o sinal "Get". A classe usa uma seção crítica para serializar operações de enfileiramento entre vários threads.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




