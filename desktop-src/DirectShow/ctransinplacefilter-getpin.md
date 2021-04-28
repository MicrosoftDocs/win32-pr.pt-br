---
description: Método CTransInPlaceFilter. GetPin – o método GetPin recupera um PIN.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Método CTransInPlaceFilter. GetPin (TRANSip. h)
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
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084764"
---
# <a name="ctransinplacefiltergetpin-method"></a>Método CTransInPlaceFilter. GetPin

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

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN ou **NULL** se o método falhar.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) . Na primeira vez que o método é chamado, ele cria ambos os Pins.

Esse método não incrementa a contagem de referência no PIN retornado, portanto, o PIN retornado não tem uma contagem de referência pendente. Se o chamador precisar manter uma referência no PIN, ele deverá chamar o método **IUnknown:: AddRef** no PIN.

Se o filtro usar os Pins [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) padrão, você provavelmente não precisará substituir esse método. No entanto, se o filtro usar Pins que estendam essas classes, você deverá substituir esse método para criar Pins desse tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




