---
description: O método EndOfStream é chamado depois que o objeto entrega a última amostra. A classe derivada deve implementar esse método.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Método CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782254"
---
# <a name="cpullpinendofstream-method"></a>Método CPullPin. EndOfStream

O `EndOfStream` método é chamado depois que o objeto entrega o último exemplo. A classe derivada deve implementar esse método.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Use este método para chamar [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) em cada PIN de entrada downstream que recebe dados desse objeto. Se os Pins de saída do filtro derivarem de [**CBaseOutputPin**](cbaseoutputpin.md), chame o método [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




