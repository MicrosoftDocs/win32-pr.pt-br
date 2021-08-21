---
description: Identificador para o thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Membro CAMThread:: m_hThread (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7293a97373a53d102887e5958c4296aff3dcfe3d392c80492ed773af62a8f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158907"
---
# <a name="camthreadm_hthread-member"></a>Membro de CAMThread:: m \_ hThread

Identificador para o thread.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Comentários

Esta variável foi inicializada como **nula**. O método [**CAMThread:: Create**](camthread-create.md) define essa variável como o identificador de thread. Para determinar se o thread existe, chame o método [**CAMThread:: ThreadExists**](camthread-threadexists.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




