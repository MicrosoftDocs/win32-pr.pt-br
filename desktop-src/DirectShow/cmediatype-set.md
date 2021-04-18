---
description: O método CMediaType. Set (mtype. h) define o tipo de mídia de outro tipo de mídia. O método usa o parâmetro ' cmtype '.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Método CMediaType. Set (mtype. h)-cmtype [REF] parâmetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105756620"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Método CMediaType. Set (mtype. h)-cmtype [REF] parâmetro

O `Set` método define o tipo de mídia de outro tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cmtype* \[ referência\]
</dt> <dd>

Referência a um objeto [**CMediaType**](cmediatype.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método copia todo o tipo de mídia de *cmtype*.

## <a name="requirements"></a>Requisitos

| Requisito                   | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Mtype. h (incluir fluxos. h)                                                                                     |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




