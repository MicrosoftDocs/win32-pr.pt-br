---
description: Método CTransInPlaceInputPin.CheckMediaType – o método CheckMediaType determina se o pin aceita um tipo de mídia específico.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Método CTransInPlaceInputPin.CheckMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91a1889e9c8a4060b734449df9f73474c16d1aec09d6534de048359ced156958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654838"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>Método CTransInPlaceInputPin.CheckMediaType

O `CheckMediaType` método determina se o pin aceita um tipo de mídia específico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o tipo de mídia proposto for aceitável. Caso contrário, retornará S \_ FALSE ou um código de erro.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CTransformInputPin::CheckMediaType.**](ctransforminputpin-checkmediatype.md) Ele chama o método [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de entrada. Se o pino de saída estiver conectado, esse método também chamará o [**método IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




