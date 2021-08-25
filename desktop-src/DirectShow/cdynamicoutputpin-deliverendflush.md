---
description: Método CDynamicOutputPin.DeliverEndFlush – o método DeliverEndFlush solicita o pino de entrada conectado para encerrar uma operação de liberação.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin.DeliverEndFlush (Amfilter.h)
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
ms.openlocfilehash: 4cdd7e26b0c08b154c6cffd08066e8ae841a6aa849db4751ffa0cdf252848719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055946"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Método CDynamicOutputPin.DeliverEndFlush

O `DeliverEndFlush` método solicita o pino de entrada conectado para encerrar uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa da falha.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md) Ele redefine o [**evento CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




