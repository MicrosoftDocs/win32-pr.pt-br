---
description: 'O método CMediaType. CMediaType:: Operator = (mtype. h) sobrecarrega o operador de atribuição para copiar um tipo de mídia.'
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType:: Operator = Method (mtype. h)-parâmetro cmtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105759136"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a>CMediaType. CMediaType:: Operator = Method (mtype. h)-parâmetro cmtype

Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cmtype* \[ referência\]
</dt> <dd>

Referência a um objeto **CMediaType** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos

| Requisito                   | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Mtype. h (incluir fluxos. h)                                                                                     |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




