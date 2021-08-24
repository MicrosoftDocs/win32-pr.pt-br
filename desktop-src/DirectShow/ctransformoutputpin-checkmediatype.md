---
description: Método CTransformOutputPin.CheckMediaType – o método CheckMediaType determina se o pin aceita um tipo de mídia específico.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Método CTransformOutputPin.CheckMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3894e701b22f6380e591eccf978e84a1321f57a84485cea8a6e3116181f3f2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538456"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>Método CTransformOutputPin.CheckMediaType

O `CheckMediaType` método determina se o pin aceita um tipo de mídia específico.

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

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O pino de entrada do filtro não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método implementa o método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtual puro. O método falhará se o pino de entrada do filtro não estiver conectado. Caso contrário, ele chamará o método [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) do filtro, que também é virtual puro. A classe derivada do filtro deve implementar **CheckTransform,** que determina se o tipo de mídia de saída proposto é compatível com o tipo de mídia de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




