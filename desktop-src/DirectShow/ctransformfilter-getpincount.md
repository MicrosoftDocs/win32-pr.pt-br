---
description: O método GetPinCount recupera o número de pinos no filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Método CTransformFilter.GetPinCount (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9269149d7f2bbc95e811515f70aa279a4aafd8cf34b2d5077ed69019b86c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953595"
---
# <a name="ctransformfiltergetpincount-method"></a>Método CTransformFilter.GetPinCount

O `GetPinCount` método recupera o número de pinos no filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna 2.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseFilter::GetPinCount.**](cbasefilter-getpincount.md) A **classe CTransformFilter** dá suporte a exatamente um pino de entrada e um pino de saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




