---
description: Método CTransformFilter.EndFlush – o método EndFlush encerra uma operação de liberação.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Método CTransformFilter.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 593ce39dbba6ccf90838b4847bb0a548b67e4785bb21d3f299882e1eecdf8394
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083906"
---
# <a name="ctransformfilterendflush-method"></a>Método CTransformFilter.EndFlush

O `EndFlush` método encerra uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT.**

## <a name="remarks"></a>Comentários

No final de uma operação de liberação, o método [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) do pino de entrada chama esse método. Esse método passa a `EndFlush` chamada downstream.

Se a classe derivada usar um thread de trabalho para fornecer exemplos, ela deverá descartar todos os dados na fila antes de enviar a `EndFlush` chamada downstream. Para obter mais informações, consulte [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




