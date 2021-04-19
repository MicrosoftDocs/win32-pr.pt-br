---
description: A função EqualPins verifica se dois Pins estão no mesmo objeto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Função EqualPins (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782849"
---
# <a name="equalpins-function"></a>Função EqualPins

A função EqualPins verifica se dois Pins estão no mesmo objeto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin1* 
</dt> <dd>

Ponteiro para um PIN.

</dd> <dt>

*pPin2* 
</dt> <dd>

Ponteiro para o outro PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se ambos os Pins estiverem no mesmo objeto ou **false** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




