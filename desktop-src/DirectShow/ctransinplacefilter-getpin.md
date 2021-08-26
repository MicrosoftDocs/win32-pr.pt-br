---
description: Método CTransInPlaceFilter.GetPin – o método GetPin recupera um pin.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Método CTransInPlaceFilter.GetPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4bef01168eb7bad9a1ffc8e5e8555ecd5e8804893269723c8dba72a066b3c50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079276"
---
# <a name="ctransinplacefiltergetpin-method"></a>Método CTransInPlaceFilter.GetPin

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

Esse método substitui o [**método CTransformFilter::GetPin.**](ctransformfilter-getpin.md) Na primeira vez que o método é chamado, ele cria os dois pinos.

Esse método não incrementa a contagem de referência no pin retornado, portanto, o pino retornado não tem uma contagem de referência pendente. Se o chamador precisar manter uma referência no pino, ele deverá chamar o método **IUnknown::AddRef** no pino.

Se o filtro usar os pinos [**padrão CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin,**](ctransinplaceoutputpin.md) você provavelmente não precisará substituir esse método. Se o filtro usar pinos que estendem essas classes, no entanto, você deverá substituir esse método para criar pinos desse tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




