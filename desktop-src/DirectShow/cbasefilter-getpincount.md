---
description: Método CBaseFilter. GetPinCount – o método GetPinCount recupera o número de Pins.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Método CBaseFilter. GetPinCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7d136b5b3bbdcd8a6b21fcbd9f854de7a78a91be87a199c990e294ce8b28fb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640476"
---
# <a name="cbasefiltergetpincount-method"></a>Método CBaseFilter. GetPinCount

O `GetPinCount` método recupera o número de Pins.

## <a name="syntax"></a>Sintaxe


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o número de Pins.

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método virtual puro. Retornar o número de Pins disponíveis no momento neste filtro. Os filtros podem criar ou destruir Pins dinamicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




