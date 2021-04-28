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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094804"
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
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




