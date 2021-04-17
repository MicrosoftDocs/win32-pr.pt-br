---
description: Método destruidor.
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
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750912"
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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




