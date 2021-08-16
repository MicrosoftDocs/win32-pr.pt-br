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
ms.openlocfilehash: 0cdb3073d1dd8055986b905d6e8f50967a304e5f294b0ffcaeddcd50d8c0ee33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432506"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Método CBaseControlWindow. GetOwnerWindow

O `GetOwnerWindow` método recupera o identificador de janela de propriedade, **m \_ hwndOwner**.

## <a name="syntax"></a>Sintaxe


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a janela do proprietário.

## <a name="remarks"></a>Comentários

Recupera a janela proprietária sem chamar o método de interface. Use essa função de membro em vez de [**CBaseControlWindow:: get \_ proprietário**](cbasecontrolwindow-get-owner.md), a menos que você esteja chamando isso externamente por meio do método [**IVideoWindow:: get \_ proprietário**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




