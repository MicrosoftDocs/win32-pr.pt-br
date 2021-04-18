---
description: O método OutputPin recupera um ponteiro para o pino de saída do filtro.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Método CTransInPlaceFilter. OutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778442"
---
# <a name="ctransinplacefilteroutputpin-method"></a>Método CTransInPlaceFilter. OutputPin

O `OutputPin` método recupera um ponteiro para o pino de saída do filtro.

## <a name="syntax"></a>Sintaxe


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a variável de membro [**CTransformFilter:: m \_ pOutput**](ctransformfilter-m-poutput.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




