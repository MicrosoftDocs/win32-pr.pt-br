---
description: O método GetSourceRect recupera o retângulo de origem atual.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Método CDrawImage. GetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787411"
---
# <a name="cdrawimagegetsourcerect-method"></a>Método CDrawImage. GetSourceRect

O `GetSourceRect` método recupera o retângulo de origem atual.

## <a name="syntax"></a>Sintaxe


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Ponteiro para uma estrutura **Rect** que recebe o retângulo de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




