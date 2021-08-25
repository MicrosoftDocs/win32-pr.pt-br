---
description: Método CTransformFilter.GetPin – o método GetPin recupera um pino.
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Método CTransformFilter.GetPin (Transfrm.h)
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
ms.openlocfilehash: 32f9ccdd2b7d787faa6f1081c51bf107b979d26d952552651542afcb34f985ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823916"
---
# <a name="ctransformfiltergetpin-method"></a>Método CTransformFilter.GetPin

O `GetPin` método recupera um pin.

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

Número do pino especificado, indexado de zero. Nesse filtro, o pino 0 é o pino de entrada e o pino 1 é o pino de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o [**objeto CBasePin**](cbasepin.md) que implementa o pino ou **NULL** se o método falhar.

## <a name="remarks"></a>Comentários

Esse método implementa o método [**CBaseFilter::GetPin**](cbasefilter-getpin.md) virtual puro. Na primeira vez que o método é chamado, ele cria os dois pinos.

Esse método não incrementa a contagem de referência no pin retornado, portanto, o pino retornado não tem uma contagem de referência pendente. Se o chamador precisar manter uma referência no pino, ele deverá chamar o método **IUnknown::AddRef** no pino.

Se o filtro usar os pinos [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) padrão, você provavelmente não precisará substituir esse método. Se o filtro usar pinos que estendem essas classes, no entanto, você deverá substituir esse método para criar pinos desse tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




