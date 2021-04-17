---
description: Prefixo de cada buffer, em bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Membro CBaseAllocator:: m_lPrefix (Amfilter. h)'
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
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755397"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Membro de CBaseAllocator:: m \_ lPrefix

Prefixo de cada buffer, em bytes. Se o valor for diferente de zero, cada ponteiro de buffer retornado pelo método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) será precedido por um bloco de bytes de tamanho *m \_ lPrefix*. Esse bloco de memória é chamado de *prefixo*. A variável de membro [**CBaseAllocator:: m \_ lSize**](cbaseallocator-m-lsize.md) não inclui o valor de prefixo.

## <a name="syntax"></a>Syntax


```C++
long m_lPrefix;
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

 

 




