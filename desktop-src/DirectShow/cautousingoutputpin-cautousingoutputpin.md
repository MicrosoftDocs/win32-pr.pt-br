---
description: Método de construtor. O construtor obtém acesso ao PIN especificado.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Construtor CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756210"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Construtor CAutoUsingOutputPin. CAutoUsingOutputPin

Método de construtor. O construtor obtém acesso ao PIN especificado.

## <a name="syntax"></a>Sintaxe


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Ponteiro para um objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que contém um valor **HRESULT** . O valor deve ser S \_ OK.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o método retorna, o valor de *\* PHR* indica o êxito ou a falha do método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




