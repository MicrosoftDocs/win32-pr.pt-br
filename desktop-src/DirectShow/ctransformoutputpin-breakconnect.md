---
description: Método CTransformOutputPin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Método CTransformOutputPin. BreakConnect (Transfrm. h)
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
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084954"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>Método CTransformOutputPin. BreakConnect

O `BreakConnect` método libera o PIN de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseOutputPin:: BreakConnect**](cbaseoutputpin-breakconnect.md) . Ele chama o método [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) do filtro, que retorna s \_ OK na classe base. A classe derivada pode substituir o método **CTransformFilter:: BreakConnect** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




