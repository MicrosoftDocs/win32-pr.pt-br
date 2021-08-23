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
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017594"
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
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




