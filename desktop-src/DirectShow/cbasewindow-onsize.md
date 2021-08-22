---
description: O método OnSize manipula mensagens de tamanho do WM \_ .
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Método CBaseWindow. OnSize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c7793af3cb7866ddaaaae8823acd91ed10ac71d939af8bc9e71eff768d75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657651"
---
# <a name="cbasewindowonsize-method"></a>Método CBaseWindow. OnSize

O `OnSize` método manipula mensagens de tamanho do WM \_ .

## <a name="syntax"></a>Sintaxe


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Largura* 
</dt> <dd>

Largura da área do cliente, em pixels.

</dd> <dt>

*Altura* 
</dt> <dd>

Altura da área do cliente, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true**.

## <a name="remarks"></a>Comentários

Esse método armazena a nova largura e altura. Para recuperar esses valores, chame os métodos [**CBaseWindow:: GetWindowHeight**](cbasewindow-getwindowheight.md) e [**CBaseWindow:: GetWindowWidth**](cbasewindow-getwindowwidth.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




