---
description: O método UsingDifferentAllocators determina se os Pins de entrada e de saída estão usando alocadores diferentes.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Método CTransInPlaceFilter. UsingDifferentAllocators (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752682"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>Método CTransInPlaceFilter. UsingDifferentAllocators

O `UsingDifferentAllocators` método determina se os Pins de entrada e de saída estão usando alocadores diferentes.

## <a name="syntax"></a>Sintaxe


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará **true** se os Pins de entrada e saída estiverem usando alocadores diferentes ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




