---
description: O método de alocação aloca memória para os buffers.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Método CMemAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748439"
---
# <a name="cmemallocatoralloc-method"></a>Método CMemAllocator. Alloc

O `Alloc` método aloca memória para os buffers.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memória insuficiente.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Os requisitos de buffer não foram definidos.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) . Ele aloca um bloco contíguo de memória suficiente para os requisitos de buffer fornecidos no método [**CMemAllocator:: SetProperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




