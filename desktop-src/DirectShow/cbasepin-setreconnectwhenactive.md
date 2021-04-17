---
description: O método SetReconnectWhenActive especifica se o PIN dá suporte a reconexões dinâmicas.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Método CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783203"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>Método CBasePin. SetReconnectWhenActive

O `SetReconnectWhenActive` método especifica se o PIN dá suporte a reconexões dinâmicas.

## <a name="syntax"></a>Sintaxe


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCanReconnect* 
</dt> <dd>

Valor booliano que especifica se o PIN pode se reconectar dinamicamente. Se **for true**, o PIN poderá se reconectar dinamicamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Por padrão, você deve interromper um filtro antes de reconectar qualquer um de seus Pins. Se o PIN puder se reconectar enquanto o filtro estiver ativo, chame esse método com um valor de **true**. Para obter mais informações, consulte [criação de grafo dinâmico](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




