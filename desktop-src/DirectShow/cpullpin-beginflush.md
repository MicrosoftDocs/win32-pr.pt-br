---
description: O método BeginFlush informa o filtro proprietário para liberar os filtros downstream. A classe derivada deve implementar esse método.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Método CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757304"
---
# <a name="cpullpinbeginflush-method"></a>Método CPullPin. BeginFlush

O `BeginFlush` método informa o filtro proprietário para liberar os filtros downstream. A classe derivada deve implementar esse método.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CPullPin:: Seek**](cpullpin-seek.md) chama esse método. Implemente este método para chamar o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) em cada pino de entrada downstream que recebe dados desse objeto. Se os Pins de saída do filtro derivarem de [**CBaseOutputPin**](cbaseoutputpin.md), chame o método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .

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

 

 




