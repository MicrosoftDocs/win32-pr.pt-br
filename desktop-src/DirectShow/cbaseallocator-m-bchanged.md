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
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768410"
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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




