---
description: O método GetPin recupera um PIN.
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Método CTransformFilter. GetPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759089"
---
# <a name="ctransformfiltergetpin-method"></a>Método CTransformFilter. GetPin

O `GetPin` método recupera um PIN.

## <a name="syntax"></a>Sintaxe


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

Número do PIN especificado, indexado de zero. Nesse filtro, o pino 0 é o pino de entrada e o pino 1 é o pino de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN ou **NULL** se o método falhar.

## <a name="remarks"></a>Comentários

Esse método implementa o método puramente virtual [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) . Na primeira vez que o método é chamado, ele cria ambos os Pins.

Esse método não incrementa a contagem de referência no PIN retornado, portanto, o PIN retornado não tem uma contagem de referência pendente. Se o chamador precisar manter uma referência no PIN, ele deverá chamar o método **IUnknown:: AddRef** no PIN.

Se o filtro usar os Pins [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) padrão, você provavelmente não precisará substituir esse método. No entanto, se o filtro usar Pins que estendam essas classes, você deverá substituir esse método para criar Pins desse tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




