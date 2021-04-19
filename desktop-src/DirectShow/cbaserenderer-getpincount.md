---
description: O método GetPinCount recupera o número de Pins.
ms.assetid: 518de15d-2ecf-425e-b4cd-14aaaf938417
title: Método CBaseRenderer. GetPinCount (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71b3703389019e2217a595884ac983e90835cdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756636"
---
# <a name="cbaserenderergetpincount-method"></a>Método CBaseRenderer. GetPinCount

O `GetPinCount` método recupera o número de Pins.

## <a name="syntax"></a>Sintaxe


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna 1.

## <a name="remarks"></a>Comentários

Esse método implementa o método [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) , que é puro virtual na classe **CBaseFilter** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




