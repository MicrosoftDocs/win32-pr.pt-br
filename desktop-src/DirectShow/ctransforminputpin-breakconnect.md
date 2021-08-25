---
description: Método CTransformInputPin.BreakConnect – o método BreakConnect libera o pino de uma conexão.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Método CTransformInputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad97061bda8ec4703464d21ad4817cfd97740f4a98904255150ce75fba37c425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812886"
---
# <a name="ctransforminputpinbreakconnect-method"></a>Método CTransformInputPin.BreakConnect

O `BreakConnect` método libera o pino de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT.**

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseInputPin::BreakConnect.**](cbaseinputpin-breakconnect.md) Ele chama o método [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) do filtro, que retorna S \_ OK na classe base. A classe derivada pode substituir o **método CTransformFilter::BreakConnect.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




