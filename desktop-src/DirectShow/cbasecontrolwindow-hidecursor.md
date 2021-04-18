---
description: O método HideCursor oculta ou exibe o cursor.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Método CBaseControlWindow. HideCursor (Ctlutil. h)
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
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750077"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>Método CBaseControlWindow. HideCursor

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

Valor que especifica se o cursor deve ser mostrado. Defina como OATRUE para ocultar o cursor ou OAFALSE para exibir o cursor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




