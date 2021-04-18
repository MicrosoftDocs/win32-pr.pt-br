---
description: O método PossiblyEatMessage encaminha as mensagens de teclado e mouse para a janela de drenagem de mensagem.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Método CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756204"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>Método CBaseControlWindow. PossiblyEatMessage

O `PossiblyEatMessage` método encaminha as mensagens de teclado e mouse para a janela de drenagem de mensagem.

## <a name="syntax"></a>Sintaxe


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Mensagem de janela.

</dd> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro de mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se a mensagem foi encaminhada para a janela ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A janela de drenagem de mensagem é uma janela designada para receber determinadas mensagens de mouse e teclado. Inicialmente, a janela é **nula**; Ele pode ser definido chamando [**CBaseControlWindow::p UT \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).

Se a janela de drenagem de mensagem não for **nula**, `PossiblyEatMessage` o posta as seguintes mensagens nessa janela:

-   caractere do WM \_
-   DEADCHAR do WM \_
-   o WM \_ KEYDOWN
-   o WM \_ KEYUP
-   LBUTTONDBLCLK do WM \_
-   LBUTTONDOWN do WM \_
-   LBUTTONUP do WM \_
-   MBUTTONDBLCLK do WM \_
-   MBUTTONDOWN do WM \_
-   MBUTTONUP do WM \_
-   MOUSEACTIVATE do WM \_
-   admousemove do WM \_
-   NCLBUTTONDBLCLK do WM \_
-   NCLBUTTONDOWN do WM \_
-   NCLBUTTONUP do WM \_
-   NCMBUTTONDBLCLK do WM \_
-   NCMBUTTONDOWN do WM \_
-   NCMBUTTONUP do WM \_
-   NCMOUSEMOVE do WM \_
-   NCRBUTTONDBLCLK do WM \_
-   NCRBUTTONDOWN do WM \_
-   NCRBUTTONUP do WM \_
-   RBUTTONDBLCLK do WM \_
-   RBUTTONDOWN do WM \_
-   RBUTTONUP do WM \_
-   SYSCHAR do WM \_
-   SYSDEADCHAR do WM \_
-   SYSKEYDOWN do WM \_
-   SYSKEYUP do WM \_

Ele ignora outras mensagens. Se a janela de drenagem de mensagem for **nula**, o método ignorará todas as mensagens de janela. O método retornará **true** se publicar a mensagem ou **false** caso contrário. A classe **CBaseWindow** chama esse método quando recebe uma mensagem de janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




