---
description: 'Decrementa a contagem de referência no objeto. Esse método implementa o método INonDelegatingUnknown:: NonDelegatingRelease.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Método CUnknown. NonDelegatingRelease (combase. h)
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
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754217"
---
# <a name="cunknownnondelegatingrelease-method"></a>Método CUnknown. NonDelegatingRelease

Decrementa a contagem de referência no objeto. Esse método implementa o método **INonDelegatingUnknown:: NonDelegatingRelease** .

## <a name="syntax"></a>Sintaxe


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a contagem de referência.

## <a name="remarks"></a>Comentários

Quando a contagem de referência chega a zero, o objeto se exclui.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




