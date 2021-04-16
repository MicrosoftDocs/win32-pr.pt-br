---
description: O método FindPinNumber recupera o número de um PIN especificado no filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Método CSource. FindPinNumber (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779241"
---
# <a name="csourcefindpinnumber-method"></a>Método CSource. FindPinNumber

O `FindPinNumber` método recupera o número de um PIN especificado no filtro.

## <a name="syntax"></a>Sintaxe


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número do PIN ou 1 se o PIN não for encontrado neste filtro. O primeiro PIN é numerado como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




