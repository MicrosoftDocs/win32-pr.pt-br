---
description: Número de buffers a serem fornecidos.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Membro CBaseAllocator:: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c33749ee6293c301501962939e25118595db10592713fb46dc10d01083c0096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661688"
---
# <a name="cbaseallocatorm_lcount-member"></a>Membro de CBaseAllocator:: m \_ lCount

Número de buffers a serem fornecidos. O método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) define esse valor. Os buffers não são alocados até que o método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) seja chamado. O número atual de buffers alocados é especificado pela variável de membro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .

## <a name="syntax"></a>Sintaxe


```C++
long m_lCount;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




