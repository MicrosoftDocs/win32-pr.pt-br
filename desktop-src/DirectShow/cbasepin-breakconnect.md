---
description: Método CBasePin.BreakConnect – o método BreakConnect libera o pino de uma conexão.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin.BreakConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c40c7614f94b2be5e5f588a706b4b0bd1eec92c3181ffbedcad3ae1e57183f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955225"
---
# <a name="cbasepinbreakconnect-method"></a>Método CBasePin.BreakConnect

O `BreakConnect` método libera o pino de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método é chamado durante a desconexão de pino pelo [**método CBasePin::D isconnect.**](cbasepin-disconnect.md) Ele também será chamado durante uma tentativa de conexão se o [**método CBasePin::CheckConnect**](cbasepin-checkconnect.md) falhar.

Esse método deve liberar todos os recursos que foram obtidos pelo **método CheckConnect.** Por exemplo, se **CheckConnect** alocar memória, `BreakConnect` deverá liberar a memória. Se **CheckConnect** consultar o pino de conexão para uma interface, `BreakConnect` deverá liberar a interface.

Observe que `BreakConnect` pode ser chamado sem uma chamada correspondente para **CompleteConnect.** Portanto, você não pode supor **que CompleteConnect** tenha sido chamado anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




