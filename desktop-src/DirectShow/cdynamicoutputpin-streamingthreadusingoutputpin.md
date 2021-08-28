---
description: O método StreamingThreadUsingOutputPin determina se qualquer thread está executando uma operação de streaming no pino.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Método CDynamicOutputPin.StreamingThreadUsingOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4687db225a616adef6d1c756ae9295e2c273c0315f37d119c7bacd0c226233e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539716"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Método CDynamicOutputPin.StreamingThreadUsingOutputPin

O método StreamingThreadUsingOutputPin determina se qualquer thread está executando uma operação de streaming no pino.

## <a name="syntax"></a>Sintaxe


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se um thread estiver executando uma operação de streaming no pino. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Se algum thread tiver retornado com êxito do método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) e não tiver feito uma chamada correspondente para o [**método CDynamicOutputPin::StopUsingOutputPin,**](cdynamicoutputpin-stopusingoutputpin.md) esse método retornará **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




