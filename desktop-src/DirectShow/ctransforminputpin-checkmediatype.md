---
description: O método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Método CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780646"
---
# <a name="ctransforminputpincheckmediatype-method"></a>Método CTransformInputPin. CheckMediaType

O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método implementa o método puramente virtual [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) . Ele chama o método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) do filtro, que também é virtual puro. A classe derivada do filtro deve implementar **CheckInputType** para determinar se um determinado tipo de entrada é aceitável.

Se o pino de saída do filtro estiver conectado, esse método também chamará o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) do filtro para determinar se o tipo de entrada é compatível com o tipo de saída. O método **CheckTransform** também é virtual puro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




