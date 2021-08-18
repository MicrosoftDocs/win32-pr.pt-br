---
description: O método Inativo notifica o pino de que o filtro foi interrompido.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Método CDynamicOutputPin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d52ec1735be6d4e89885295a9d9c2d382142fdc9d31f95b6368d0ef2f331608e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317706"
---
# <a name="cdynamicoutputpininactive-method"></a>Método CDynamicOutputPin.Inactive

O `Inactive` método notifica o pino de que o filtro foi interrompido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa da falha.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseOutputPin::Inactive.**](cbaseoutputpin-inactive.md) Ele define o [**evento CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




