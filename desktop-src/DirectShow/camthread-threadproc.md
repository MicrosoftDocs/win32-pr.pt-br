---
description: O método ThreadProc é o procedimento de thread.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Método CAMThread. ThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750913"
---
# <a name="camthreadthreadproc-method"></a>Método CAMThread. ThreadProc

O `ThreadProc` método é o procedimento de thread.

## <a name="syntax"></a>Sintaxe


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** cujo significado é definido pela classe derivada.

## <a name="remarks"></a>Comentários

Esse é um método virtual puro. Implemente esse método em sua classe derivada para fornecer um procedimento de thread. Quando o método [**CAMThread:: Create**](camthread-create.md) cria um thread, ele fornece o endereço do método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) que, por sua vez, chama o método ThreadProc.

Normalmente, o método ThreadProc entrará em um loop que recupera solicitações (chamando os métodos [**CAMThread:: GetRequest**](camthread-getrequest.md) ou [**CAMThread:: CheckRequest**](camthread-checkrequest.md) ) e processa os dados.

Quando esse método retorna, o thread é encerrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




