---
description: A \_ variável de membro m pAlloc é um ponteiro para a interface IMemAllocator do alocador de memória.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Membro CPullPin:: m_pAlloc (Pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750466"
---
# <a name="cpullpinm_palloc-member"></a>Membro de CPullPin:: m \_ pAlloc

A `m_pAlloc` variável de membro é um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador de memória.

## <a name="syntax"></a>Sintaxe


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Comentários

O método [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) define essa variável de membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




