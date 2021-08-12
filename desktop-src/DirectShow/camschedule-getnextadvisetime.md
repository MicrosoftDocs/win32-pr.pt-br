---
description: O método GetNextAdviseTime recupera a hora da próxima solicitação de aviso.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Método CAMSchedule. GetNextAdviseTime (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c7fd04622a5cdab8bade32f41b090d8f480db292209d284804b5180134954f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662342"
---
# <a name="camschedulegetnextadvisetime-method"></a>Método CAMSchedule. GetNextAdviseTime

O `GetNextAdviseTime` método recupera a hora da próxima solicitação de aviso.

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o tempo de referência da próxima solicitação de aviso ou o tempo máximo em que \_ nenhuma solicitação é agendada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir Fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




