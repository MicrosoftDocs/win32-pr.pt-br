---
description: Diminui a contagem de referência no objeto . Esse método implementa o método INonDeltingUnknown::NonDeltingRelease.
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Método CUnknown.NonDeltingRelease (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ac5145e1776602c5bb358805c45ec271766fe918b7924d948e286ae32b31794
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821950"
---
# <a name="cunknownnondelegatingrelease-method"></a>Método CUnknown.NonDeltingRelease

Diminui a contagem de referência no objeto . Esse método implementa o **método INonDeltingUnknown::NonDeltingRelease.**

## <a name="syntax"></a>Sintaxe


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a contagem de referência.

## <a name="remarks"></a>Comentários

Quando a contagem de referência atinge zero, o objeto se exclui.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




