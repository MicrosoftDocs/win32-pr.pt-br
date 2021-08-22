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
ms.openlocfilehash: 12e59b434562e84c42228c16282620efe10866ea9dad85a4d62beb46f5a59e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688976"
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
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                                                                                             |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha. [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) não foi chamado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseOutputPin:: active**](cbaseoutputpin-active.md) . Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) . Se o filtro proprietário não tiver chamado **SetConfigInfo**, esse método retornará E \_ falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




