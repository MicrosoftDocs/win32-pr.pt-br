---
description: O método GetPinCount recupera o número de Pins no filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Método CTransformFilter. GetPinCount (Transfrm. h)
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
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751481"
---
# <a name="ctransformfiltergetpincount-method"></a>Método CTransformFilter. GetPinCount

O `GetPinCount` método recupera o número de Pins no filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna 2.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) . A classe **CTransformFilter** dá suporte a exatamente um PIN de entrada e um PIN de saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




