---
description: Método CDynamicOutputPin. active – o método ativo notifica o PIN de que o filtro está ativo agora.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Método CDynamicOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099324"
---
# <a name="cdynamicoutputpinactive-method"></a>Método CDynamicOutputPin. active

O `Active` método notifica o PIN de que o filtro está ativo agora.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                            | Descrição                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Sucesso.<br/>                                                                                             |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha. [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) não foi chamado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseOutputPin:: active**](cbaseoutputpin-active.md) . Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) . Se o filtro proprietário não tiver chamado **SetConfigInfo**, esse método retornará E \_ falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




