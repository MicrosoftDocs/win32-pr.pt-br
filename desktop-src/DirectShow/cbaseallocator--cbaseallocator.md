---
description: CBaseAllocator. ~ CBaseAllocator destruidor-método Destruitor.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator. ~ CBaseAllocator Destruitor (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89b87bd4e706e5270b49ca94d1c86a6c5a5326fd3efccb1dcc45b9681e6e2fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017554"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Destruidor CBaseAllocator. ~ CBaseAllocator

Método destruidor.

## <a name="syntax"></a>Sintaxe


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Comentários

Sempre chame o método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir o objeto. O destruidor de classe base não pode chamar **uncommit**, porque esse método chama o método virtual puro [**CBaseAllocator:: Free**](cbaseallocator-free.md). As classes derivadas devem substituir esse destruidor e chamar a **deconfirmação**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




