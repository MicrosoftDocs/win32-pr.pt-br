---
description: O método SynchronousBlockOutputPin bloqueia o PIN; Não retorna até que o PIN seja bloqueado.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Método CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
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
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757424"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>Método CDynamicOutputPin. SynchronousBlockOutputPin

O `SynchronousBlockOutputPin` método bloqueia o PIN; não retorna até que o PIN seja bloqueado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                                    | Descrição                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Êxito.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ PIN \_ já \_ bloqueados**</dt> </dl>                   | O PIN já está bloqueado em outro thread.<br/>     |
| <dl> <dt>**VFW \_ E \_ PIN \_ já \_ bloqueados neste \_ \_ \_ thread**</dt> </dl> | O PIN já está bloqueado no thread de chamada.<br/> |



 

## <a name="remarks"></a>Comentários

Não chame esse método do thread de streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




