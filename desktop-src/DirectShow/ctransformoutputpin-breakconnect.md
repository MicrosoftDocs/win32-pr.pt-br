---
description: Método CTransformOutputPin.BreakConnect – o método BreakConnect libera o pino de uma conexão.
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Método CTransformOutputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf468e9f7d9cb439cfe369e3034f76b044001b31be3fd9c7a72ca475aa77d1a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103006"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>Método CTransformOutputPin.BreakConnect

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

Esse método substitui o [**método CBaseOutputPin::BreakConnect.**](cbaseoutputpin-breakconnect.md) Ele chama o método [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) do filtro, que retorna S \_ OK na classe base. A classe derivada pode substituir o **método CTransformFilter::BreakConnect.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




