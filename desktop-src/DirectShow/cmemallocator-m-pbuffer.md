---
description: Ponteiro para o bloco de memória que contém os buffers.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: Membro CMemAllocator::m_pBuffer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa9c56c5a90c1fa3fde7dda4bca82cd3f473a591db9e2e24f0b1d141c6aa33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155978"
---
# <a name="cmemallocatorm_pbuffer-member"></a>Membro CMemAllocator::m \_ pBuffer

Ponteiro para o bloco de memória que contém os buffers.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a>Comentários

Buffers de exemplo são calculados como deslocamentos desse ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




