---
description: 'O método QueryDirection recupera a direção do PIN (entrada ou saída). Esse método implementa o método IPin:: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Método CBasePin. QueryDirection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780888"
---
# <a name="cbasepinquerydirection-method"></a>Método CBasePin. QueryDirection

O `QueryDirection` método recupera a direção do PIN (entrada ou saída). Esse método implementa o método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPinDir* 
</dt> <dd>

Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ direção de PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




