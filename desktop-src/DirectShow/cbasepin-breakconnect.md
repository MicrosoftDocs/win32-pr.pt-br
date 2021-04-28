---
description: Método CBasePin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin. BreakConnect (Amfilter. h)
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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099434"
---
# <a name="cbasepinbreakconnect-method"></a>Método CBasePin. BreakConnect

O `BreakConnect` método libera o PIN de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método é chamado durante a desconexão do PIN pelo método [**CBasePin::D isconnect**](cbasepin-disconnect.md) . Ele também será chamado durante uma tentativa de conexão se o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) falhar.

Esse método deve liberar todos os recursos que foram obtidos pelo método **CheckConnect** . Por exemplo, se **CheckConnect** alocar memória, `BreakConnect` o deve liberar a memória. Se **CheckConnect** consulta o PIN de conexão de uma interface, `BreakConnect` o deve liberar a interface.

Observe que `BreakConnect` pode ser chamado sem uma chamada correspondente para **CompleteConnect**. Portanto, você não pode supor que **CompleteConnect** foi chamado anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




