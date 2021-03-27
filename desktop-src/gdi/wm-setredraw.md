---
description: Um aplicativo envia a \_ mensagem de redesenho do WM para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Mensagem de WM_SETREDRAW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170527"
---
# <a name="wm_setredraw-message"></a>Mensagem de reemissão do WM \_

Um aplicativo envia a mensagem de **\_ redesenho do WM** para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.

Para enviar essa mensagem, chame a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com os parâmetros a seguir.


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O estado de redesenho. Se esse parâmetro for **true**, o conteúdo poderá ser redesenhado após uma alteração. Se esse parâmetro for **false**, o conteúdo não poderá ser redesenhado após uma alteração.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo retornará zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Essa mensagem poderá ser útil se um aplicativo precisar adicionar vários itens a uma caixa de listagem. O aplicativo pode chamar essa mensagem com *wParam* definido como **false**, adicionar os itens e, em seguida, chamar a mensagem novamente com *wParam* definido como **true**. Por fim, o aplicativo pode chamar [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **NULL**, **NULL**, RDW \_ apagar \| RDW \_ quadro \| RDW \_ invalidar \| RDW \_ filhos) para fazer com que a caixa de listagem seja repintada.

> [!Note]  
> [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) com os sinalizadores especificados é usado em vez de [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) porque o primeiro é necessário para alguns controles que têm uma área não cliente por conta própria ou que têm estilos de janela que fazem com que eles recebam uma área que não seja de cliente (como **WS \_ THICKFRAME**, **WS \_ Border** ou **WS \_ ex \_ CLIENTEDGE**). Se o controle não tiver uma área que não seja cliente, **RedrawWindow** com esses sinalizadores fará apenas a invalidação que o **InvalidateRect** faria.

 

Se o aplicativo enviar a mensagem de **\_ reemissão do WM** para uma janela oculta, a janela ficará visível (ou seja, o sistema operacional adicionará o estilo **WS \_ visível** à janela).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de pintura e desenho](painting-and-drawing.md)
</dt> <dt>

[Pintura e desenho de mensagens](painting-and-drawing-messages.md)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
