---
description: Seção crítica que impede que o thread seja acessado por outros threads.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Membro CAMThread:: m_AccessLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757899"
---
# <a name="camthreadm_accesslock-member"></a>Membro de CAMThread:: m \_ AccessLock

Seção crítica que impede que o thread seja acessado por outros threads.

## <a name="syntax"></a>Sintaxe


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Comentários

Os métodos [**CAMThread:: Create**](camthread-create.md) e [**CAMThread:: CallWorker**](camthread-callworker.md) mantêm esse bloqueio para serializar operações no thread.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




