---
description: O método AsynchronousBlockOutputPin bloqueia o PIN. O método pode retornar antes de o PIN ser bloqueado.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Método CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752290"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>Método CDynamicOutputPin. AsynchronousBlockOutputPin

O `AsynchronousBlockOutputPin` método bloqueia o PIN. O método pode retornar antes de o PIN ser bloqueado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hNotifyCallerPinBlockedEvent* 
</dt> <dd>

Identificador para um evento. O evento é sinalizado quando o pino de saída é bloqueado ou se o chamador cancela a operação de bloqueio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                                    | Descrição                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Êxito.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ PIN \_ já \_ bloqueados**</dt> </dl>                   | O PIN já está bloqueado em outro thread.<br/>     |
| <dl> <dt>**VFW \_ E \_ PIN \_ já \_ bloqueados neste \_ \_ \_ thread**</dt> </dl> | O PIN já está bloqueado no thread de chamada.<br/> |



 

## <a name="remarks"></a>Comentários

Não chame esse método do thread de streaming.

Se nenhum thread de streaming estiver usando o PIN, esse método bloqueará imediatamente o PIN. Caso contrário, ele define o status do PIN como "Pending" e retorna. Quando a operação de streaming é concluída, o thread de streaming chama o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , que bloqueia o PIN e sinaliza o evento **hNotifyCallerPinBlockedEvent** . Para cancelar um bloco pendente, chame o método [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




