---
description: O método HideCursor oculta ou exibe o cursor.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Método CBaseControlWindow.HideCursor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6421a650471d0954031433db3814e8453cbc82586c7f37608ae947e7301c6969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158377"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>Método CBaseControlWindow.HideCursor

O `HideCursor` método oculta ou exibe o cursor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HideCursor* 
</dt> <dd>

Valor que especifica se o cursor deve ser mostrado. De definido como OATRUE para ocultar o cursor ou OAFALSE para exibir o cursor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




