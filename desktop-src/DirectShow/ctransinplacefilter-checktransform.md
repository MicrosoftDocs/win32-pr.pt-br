---
description: 'O método CheckTransform verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída. Esse método substitui o método CTransformFilter:: CheckTransform.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Método CTransInPlaceFilter. CheckTransform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49b7f4aaac21cf6a55360e2e1b970bd9dfa62c0422241f7356871117e138d57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654955"
---
# <a name="ctransinplacefilterchecktransform-method"></a>Método CTransInPlaceFilter. CheckTransform

O `CheckTransform` método verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída. Esse método substitui o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de entrada.

</dd> <dt>

*mtOut* 
</dt> <dd>

Ponteiro para um objeto **CMediaType** que especifica o tipo de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O filtro **CTransInPlace** nunca chama `CheckTransform` . Em vez disso, toda a conexão de PIN usa [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) para verificar o tipo de mídia, com a suposição de que os tipos de entrada e saída sempre correspondem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




