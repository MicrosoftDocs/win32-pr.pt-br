---
description: O método SynchronousBlockOutputPin bloqueia o pino; não retorna até que o pino seja bloqueado.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Método CDynamicOutputPin.SynchronousBlockOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8613a27d8af2dc2b69a93a1f324db17b054cf2dd312fdb0c9d6cd63e6c89ca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916306"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>Método CDynamicOutputPin.SynchronousBlockOutputPin

O `SynchronousBlockOutputPin` método bloqueia o pino; não retorna até que o pino seja bloqueado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                                                    | Descrição                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Êxito.<br/>                                      |
| <dl> <dt>**PIN DO VFW \_ E \_ JÁ \_ \_ BLOQUEADO**</dt> </dl>                   | O pin já está bloqueado em outro thread.<br/>     |
| <dl> <dt>**VFW \_ E PIN JÁ \_ \_ \_ \_ \_ BLOQUEADOS NESSE \_ THREAD**</dt> </dl> | O pin já está bloqueado no thread de chamada.<br/> |



 

## <a name="remarks"></a>Comentários

Não chame esse método do thread de streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




