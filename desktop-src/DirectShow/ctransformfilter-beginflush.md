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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085154"
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

Se a classe derivada usar um thread de trabalho para fornecer amostras, ela deverá descartar todos os dados na fila durante uma operação de liberação. Isso pode ser feito no `BeginFlush` método ou no método [**EndFlush**](ctransformfilter-endflush.md) . No entanto, observe que `BeginFlush` as chamadas para não estão sincronizadas com o thread de streaming. Se o `BeginFlush` método descartar os dados na fila, o filtro deverá ter cuidado para não processar mais dados entre as `BeginFlush` chamadas e **EndFlush** . Para obter mais informações, consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




