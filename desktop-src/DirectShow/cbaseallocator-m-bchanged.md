---
description: Sinalizador que indica se os requisitos de buffer foram alterados.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Membro CBaseAllocator:: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7edb5ed770628d7dfd982017e720ef0136bace74dd7e311121925f6c8657d2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131496"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Membro de CBaseAllocator:: m \_ bChanged

Sinalizador que indica se os requisitos de buffer foram alterados. O método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) define o valor como **true**. Em uma classe derivada, o método virtual puro [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) deve definir o valor de volta como **false**. Depois que os buffers forem alocados, não será necessário realocá-los enquanto *m \_ BChanged* for **false**.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bChanged;
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

 

 




