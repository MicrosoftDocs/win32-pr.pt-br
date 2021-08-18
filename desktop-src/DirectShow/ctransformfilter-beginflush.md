---
description: Método CTransformFilter. BeginFlush-o método BeginFlush inicia uma operação de liberação.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Método CTransformFilter. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be20231cf62148e3487aef405735f764bf5c02b7cbaadba3c140728b66bd5391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053856"
---
# <a name="ctransformfilterbeginflush-method"></a>Método CTransformFilter. BeginFlush

O `BeginFlush` método inicia uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

No início de uma operação de liberação, o método [**CTransformInputPin:: BeginFlush**](ctransforminputpin-beginflush.md) do pino de entrada chama esse método. Esse método passa a `BeginFlush` chamada downstream.

Se a classe derivada usar um thread de trabalho para fornecer amostras, ela deverá descartar todos os dados na fila durante uma operação de liberação. Isso pode ser feito no `BeginFlush` método ou no método [**EndFlush**](ctransformfilter-endflush.md) . No entanto, observe que `BeginFlush` as chamadas para não estão sincronizadas com o thread de streaming. Se o `BeginFlush` método descartar os dados na fila, o filtro deverá ter cuidado para não processar mais dados entre as `BeginFlush` chamadas e **EndFlush** . para obter mais informações, consulte [Data Flow para os desenvolvedores de filtro](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




