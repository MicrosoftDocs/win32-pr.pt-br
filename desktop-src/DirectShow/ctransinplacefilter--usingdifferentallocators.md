---
description: O método UsingDifferentAllocators determina se os pinos de entrada e saída estão usando alocadores diferentes.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Método CTransInPlaceFilter.UsingDifferentAllocators (Transip.h)
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
ms.openlocfilehash: 0033c0f5ded1fe741d27397078367049d72061c40a993833f714686d9f8a96fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953415"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>Método CTransInPlaceFilter.UsingDifferentAllocators

O `UsingDifferentAllocators` método determina se os pinos de entrada e saída estão usando alocadores diferentes.

## <a name="syntax"></a>Sintaxe


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se os pinos de entrada e saída estão usando alocadores diferentes ou **FALSE** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




