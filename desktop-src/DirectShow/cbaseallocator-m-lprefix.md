---
description: Prefixo de cada buffer, em bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: Membro CBaseAllocator::m_lPrefix (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a22f2ac1a54c4820f109b55002428c87df321328ef6b6b6d6096343df8cde85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955285"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Membro CBaseAllocator::m \_ lPrefix

Prefixo de cada buffer, em bytes. Se o valor for diferente de zero, cada ponteiro de buffer retornado pelo método [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) será precedido por um bloco de bytes de *tamanho m \_ lPrefix*. Esse bloco de memória é chamado de *prefixo*. A [**variável de membro CBaseAllocator::m \_ lSize**](cbaseallocator-m-lsize.md) não inclui o valor do prefixo.

## <a name="syntax"></a>Syntax


```C++
long m_lPrefix;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




