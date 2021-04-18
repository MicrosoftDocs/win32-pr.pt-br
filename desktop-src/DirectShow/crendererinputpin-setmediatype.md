---
description: 'O método SetMediaType define o tipo de mídia para a conexão. Esse método substitui o método CBasePin:: SetMediaType.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Método CRendererInputPin. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753165"
---
# <a name="crendererinputpinsetmediatype-method"></a>Método CRendererInputPin. SetMediaType

O `SetMediaType` método define o tipo de mídia para a conexão. Esse método substitui o método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




