---
description: O método GetTargetRect recupera o retângulo de destino atual.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Método CDrawImage. GetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ba520b0bb48ed60ba2a9c48165eb83959107ecd777bdecc8bce12e7672d221e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076406"
---
# <a name="cdrawimagegettargetrect-method"></a>Método CDrawImage. GetTargetRect

O `GetTargetRect` método recupera o retângulo de destino atual.

## <a name="syntax"></a>Sintaxe


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Ponteiro para uma estrutura **Rect** que recebe o retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




