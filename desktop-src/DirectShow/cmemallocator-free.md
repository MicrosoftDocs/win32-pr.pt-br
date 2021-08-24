---
description: O método gratuito é chamado durante uma operação de desconfirmação.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Método CMemAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2ffea6fdd60e4053f6c00ee1c87ca9596560909864c861d46b5728dad13a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155988"
---
# <a name="cmemallocatorfree-method"></a>Método CMemAllocator. Free

O `Free` método é chamado durante uma operação de desconfirmação. Esse método implementa o método puramente virtual [**CBaseAllocator:: Free**](cbaseallocator-free.md) , mas não faz nada. A memória de buffer não é realmente liberada até que o objeto **CMemAllocator** seja destruído. O método destruidor chama [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md) para liberar a memória.

## <a name="syntax"></a>Sintaxe


```C++
void Free();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




