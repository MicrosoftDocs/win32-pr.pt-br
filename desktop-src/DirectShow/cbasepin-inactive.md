---
description: O método inativo notifica o PIN de que o filtro não está mais ativo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755362"
---
# <a name="cbasepininactive-method"></a>Método CBasePin. Inactive

O `Inactive` método notifica o PIN de que o filtro não está mais ativo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando o filtro é interrompido, a classe [**CBaseFilter**](cbasefilter.md) chama esse método em todos os Pins conectados do filtro.

Esse método não faz nada na classe base. Classes derivadas devem substituir esse método para liberar todos os recursos obtidos pelo método [**CBasePin:: active**](cbasepin-active.md) ; por exemplo, para desconfirmar os alocadores do PIN.

O estado interno do Gerenciador de grafo de filtro não é atualizado até que esse método retorne, portanto, não teste o estado desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




