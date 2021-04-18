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
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749052"
---
# <a name="cbaseallocatorm_lcount-member"></a>Membro de CBaseAllocator:: m \_ lCount

Número de buffers a serem fornecidos. O método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) define esse valor. Os buffers não são alocados até que o método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) seja chamado. O número atual de buffers alocados é especificado pela variável de membro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .

## <a name="syntax"></a>Syntax


```C++
long m_lCount;
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

 

 




