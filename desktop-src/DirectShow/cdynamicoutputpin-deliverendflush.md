---
description: Método CDynamicOutputPin. DeliverEndFlush – o método DeliverEndFlush solicita o pino de entrada conectado para finalizar uma operação de liberação.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095704"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Método CDynamicOutputPin. DeliverEndFlush

O `DeliverEndFlush` método solicita o PIN de entrada conectado para finalizar uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) . Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




