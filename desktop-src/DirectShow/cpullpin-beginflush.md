---
description: O método BeginFlush informa o filtro de propriedade para liberar os filtros downstream. A classe derivada deve implementar esse método.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Método CPullPin.BeginFlush (Pullpin.h)
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
ms.openlocfilehash: d2c7998c1c38a533d67edcd2cc237188a627ec8258a8b0349066e31ecf0fbaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687746"
---
# <a name="cpullpinbeginflush-method"></a>Método CPullPin.BeginFlush

O `BeginFlush` método informa o filtro de propriedade para liberar os filtros downstream. A classe derivada deve implementar esse método.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

O [**método CPullPin::Seek**](cpullpin-seek.md) chama esse método. Implemente esse método para chamar o [**método IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) em cada pino de entrada downstream que recebe dados desse objeto. Se os pins de saída do filtro derivam de [**CBaseOutputPin,**](cbaseoutputpin.md)chame o [**método CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)

Esse design permite que o filtro busque o fluxo simplesmente chamando **Seek** no **objeto CPullPin.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




