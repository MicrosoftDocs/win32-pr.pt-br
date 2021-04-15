---
description: O método GetOwnerWindow recupera o identificador de janela de propriedade, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Método CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747417"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Método CBaseControlWindow. GetOwnerWindow

O `GetOwnerWindow` método recupera o identificador de janela de propriedade, **m \_ hwndOwner**.

## <a name="syntax"></a>Sintaxe


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a janela do proprietário.

## <a name="remarks"></a>Comentários

Recupera a janela proprietária sem chamar o método de interface. Use essa função de membro em vez de [**CBaseControlWindow:: get \_ proprietário**](cbasecontrolwindow-get-owner.md), a menos que você esteja chamando isso externamente por meio do método [**IVideoWindow:: get \_ proprietário**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




