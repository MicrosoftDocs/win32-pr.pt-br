---
description: O método CanReconnectWhenActive consulta se o PIN dá suporte a reconexões dinâmicas.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Método CBasePin. CanReconnectWhenActive (Amfilter. h)
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
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753356"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>Método CBasePin. CanReconnectWhenActive

O `CanReconnectWhenActive` método consulta se o PIN dá suporte a reconexões dinâmicas.

## <a name="syntax"></a>Sintaxe


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor booliano que especifica se o PIN pode se reconectar dinamicamente. Se **for true**, o PIN poderá se reconectar dinamicamente.

## <a name="remarks"></a>Comentários

Por padrão, você deve interromper um filtro antes de reconectar qualquer um de seus Pins. No entanto, se um PIN oferecer suporte à reconexão dinâmica, ele poderá se reconectar enquanto o filtro estiver ativo. Para obter mais informações, consulte [criação de grafo dinâmico](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




