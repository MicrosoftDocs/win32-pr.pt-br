---
description: O método PossiblyEatMessage encaminha mensagens de teclado e mouse para a janela de esgotamento de mensagens.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Método CBaseControlWindow.PossiblyEatMessage (Ctlutil.h)
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
ms.openlocfilehash: 403fb4d170f9c3cf0b7d68d3ac6ce1fdcc9c81a14b1c76d74e67bb64d4d9cc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017334"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>Método CBaseControlWindow.PossiblyEatMessage

O `PossiblyEatMessage` método encaminha mensagens de teclado e mouse para a janela de esgotamento de mensagens.

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

*Umsg* 
</dt> <dd>

Mensagem da janela.

</dd> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro de mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a mensagem tiver sido encaminhada para a janela ou **FALSE** caso contrário.

## <a name="remarks"></a>Comentários

A janela de esgotamento de mensagens é uma janela designada para receber determinadas mensagens do mouse e do teclado. Inicialmente, a janela é **NULL;** ele pode ser definido chamando [**CBaseControlWindow::p ut \_ MessageDbase.**](cbasecontrolwindow-put-messagedrain.md)

Se a janela de esgotamento de mensagens for não **NULL,** `PossiblyEatMessage` poste as seguintes mensagens nessa janela:

-   WM \_ CHAR
-   WM \_ DEADCHAR
-   WM \_ KEYDOWN
-   WM \_ KEYUP
-   WM \_ LBUTTONDBLCLK
-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDBLCLK
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEACTIVATE
-   WM \_ MOUSEMOVE
-   WM \_ NCLBUTTONDBLCLK
-   WM \_ NCLBUTTONDOWN
-   WM \_ NCLBUTTONUP
-   WM \_ NCMBUTTONDBLCLK
-   WM \_ NCMBUTTONDOWN
-   WM \_ NCMBUTTONUP
-   WM \_ NCMOUSEMOVE
-   WM \_ NCRBUTTONDBLCLK
-   WM \_ NCRBUTTONDOWN
-   WM \_ NCRBUTTONUP
-   WM \_ RBUTTONDBLCLK
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP
-   WM \_ SYSCHAR
-   WM \_ SYSDEADCHAR
-   WM \_ SYSKEYDOWN
-   WM \_ SYSKEYUP

Ele ignora outras mensagens. Se a janela de esgotamento de mensagens for **NULL,** o método ignorará todas as mensagens da janela. O método **retornará TRUE** se ele postar a mensagem ou **FALSE** caso contrário. A **classe CBaseWindow** chama esse método quando recebe uma mensagem de janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




