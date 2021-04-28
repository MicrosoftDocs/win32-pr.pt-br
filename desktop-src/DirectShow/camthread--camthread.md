---
description: CAMThread. ~ CAMThread destruidor-método Destruitor.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CAMThread. ~ CAMThread Destruitor (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096434"
---
# <a name="camthreadcamthread-destructor"></a>Destruidor CAMThread. ~ CAMThread

Método destruidor.

## <a name="syntax"></a>Sintaxe


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Comentários

O destruidor chama o método [**CAMThread:: Close**](camthread-close.md) , que aguarda a saída do thread.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




