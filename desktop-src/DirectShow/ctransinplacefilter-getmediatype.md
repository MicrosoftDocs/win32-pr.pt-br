---
description: Método CTransInPlaceFilter. GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial para o pino de saída.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Método CTransInPlaceFilter. GetMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079296"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>Método CTransInPlaceFilter. GetMediaType

O `GetMediaType` método recupera um tipo de mídia preferencial para o pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice baseado em zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ inesperado.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) . Na classe **CTransInPlaceFilter** , cada pino chama o PIN conectado oposto para enumerar os tipos de mídia preferenciais. O pino de entrada chama o pino de entrada do filtro downstream e o pino de saída chama o pino de saída do filtro upstream. Portanto, o método do filtro `GetMediaType` nunca é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




