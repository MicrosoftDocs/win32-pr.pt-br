---
description: CMemAllocator. ~ CMemAllocator destruidor-método Destruitor.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator. ~ CMemAllocator Destruitor (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954375"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Destruidor CMemAllocator. ~ CMemAllocator

Método destruidor.

## <a name="syntax"></a>Sintaxe


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Comentários

Esse método substitui o destruidor de classe base para chamar [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




