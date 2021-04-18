---
description: O método EndFlush informa o filtro proprietário para finalizar uma operação de liberação. A classe derivada deve implementar esse método.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Método CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780861"
---
# <a name="cpullpinendflush-method"></a>Método CPullPin. EndFlush

O `EndFlush` método informa o filtro proprietário para finalizar uma operação de liberação. A classe derivada deve implementar esse método.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CPullPin:: Seek**](cpullpin-seek.md) chama esse método. Implemente esse método para chamar o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) em cada pino de entrada downstream que recebe dados desse objeto. Se os Pins de saída do filtro derivarem de **CBaseOutputPin**, chame o método **CBaseOutputPin::D eliverendflush** .

Esse design permite que o filtro busque o fluxo simplesmente chamando **Seek** no objeto **CPullPin** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




