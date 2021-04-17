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
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784035"
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
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




