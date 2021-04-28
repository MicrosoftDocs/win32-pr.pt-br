---
description: Método CBasePin. active – o método ativo notifica o PIN de que o filtro está ativo agora.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096096"
---
# <a name="cbasepinactive-method"></a>Método CBasePin. active

O `Active` método notifica o PIN de que o filtro está ativo agora.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando o filtro vai de parado para em pausa, a classe [**CBaseFilter**](cbasefilter.md) chama esse método em todos os Pins conectados do filtro.

Esse método não faz nada na classe base. Classes derivadas podem substituir esse método; por exemplo, um PIN pode confirmar os alocadores ou obter recursos de hardware.

O estado interno do Gerenciador de grafo de filtro não é atualizado até que essa função de membro retorne, portanto, não teste o estado desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




