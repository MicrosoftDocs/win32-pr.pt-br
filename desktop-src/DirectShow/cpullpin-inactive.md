---
description: O método inativo desliga o thread de trabalho que efetua pull dos dados do pino de saída. Esse método também desconfirma o alocador.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Método CPullPin. Inactive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56307362651761dbe2bc5c0242a24f189cf14d1e820df6a5ba21bdeb9c7deb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565366"
---
# <a name="cpullpininactive-method"></a>Método CPullPin. Inactive

O `Inactive` método desliga o thread de trabalho que efetua pull dos dados do pino de saída. Esse método também desconfirma o alocador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chame esse método quando o filtro proprietário se tornar inativo. (Se o PIN de entrada deriva de [**CBasePin**](cbasepin.md), substitua o método [**CBasePin:: Inactive**](cbasepin-inactive.md) .)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




