---
description: O método ReallyFree libera a memória para os buffers.
ms.assetid: c5c5d09f-b4f2-4a06-9309-3b2a8b8f8f1f
title: Método CMemAllocator. ReallyFree (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.ReallyFree
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ad7ca95fc7a79e97e5aea79da79fb1b161911e5835509f3a2288578e068e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954355"
---
# <a name="cmemallocatorreallyfree-method"></a>Método CMemAllocator. ReallyFree

O `ReallyFree` método libera a memória para os buffers.

## <a name="syntax"></a>Sintaxe


```C++
void ReallyFree();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A classe [**CMemAllocator**](cmemallocator.md) mantém a memória até que o objeto seja excluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




