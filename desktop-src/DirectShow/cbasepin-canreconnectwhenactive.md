---
description: O método CanReconnectWhenActive consulta se o pino dá suporte a reconexões dinâmicas.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Método CBasePin.CanReconnectWhenActive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffe4cc09efa53ac4d3ab8089a1061d860206f9734c214d250b5c3cdc907eaf84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916916"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>Método CBasePin.CanReconnectWhenActive

O `CanReconnectWhenActive` método consulta se o pino dá suporte a reconexões dinâmicas.

## <a name="syntax"></a>Sintaxe


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor booliana que especifica se o pino pode se reconectar dinamicamente. Se **TRUE**, o pino poderá se reconectar dinamicamente.

## <a name="remarks"></a>Comentários

Por padrão, você deve parar um filtro antes de reconectar qualquer um de seus pinos. Se um pino dá suporte à reconexão dinâmica, no entanto, ele pode se reconectar enquanto o filtro está ativo. Para obter mais informações, consulte [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




