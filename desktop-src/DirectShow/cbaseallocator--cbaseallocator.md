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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096414"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




