---
description: Você envia a mensagem de **WM_SETREDRAW** para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Mensagem de WM_SETREDRAW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593452"
---
# <a name="wm_setredraw-message"></a>WM_SETREDRAW mensagem

Você envia a mensagem de **\_ redesenho do WM** para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.

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

`wParam`

O estado de redesenho. Se esse parâmetro for **true**, o conteúdo poderá ser redesenhado após uma alteração. Se esse parâmetro for **false**, o conteúdo não poderá ser redesenhado após uma alteração.

`lParam`

Esse parâmetro não é usado.

## <a name="return-value"></a>Retornar valor

Seu aplicativo deverá retornar 0 se processar essa mensagem.

## <a name="remarks"></a>Comentários

Essa mensagem poderá ser útil se o aplicativo precisar adicionar vários itens a uma caixa de listagem. Seu aplicativo pode chamar essa mensagem com *wParam* definido como **false**, adicionar os itens e, em seguida, chamar a mensagem novamente com *wParam* definido como **true**. Por fim, seu aplicativo pode chamar [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **NULL**, **NULL**, RDW \_ apagar \| RDW \_ quadro \| RDW \_ invalidar \| RDW \_ filhos) para fazer com que a caixa de listagem seja repintada.

> [!NOTE] 
> Você deve usar [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) com os sinalizadores especificados, em vez de [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), porque o primeiro é necessário para alguns controles que têm uma área não cliente própria ou que têm estilos de janela que fazem com que eles recebam uma área que não seja de cliente (como **WS_THICKFRAME**, **WS_BORDER** ou **WS_EX_CLIENTEDGE**). Se o controle não tiver uma área não cliente, **RedrawWindow** com esses sinalizadores fará apenas a invalidação que o **InvalidateRect** faria.

Passar uma mensagem de **WM_SETREDRAW** para a função **DefWindowProc** remove o estilo de **WS_VISIBLE** da janela quando *wParam* é definido como **false**. Embora o conteúdo da janela permaneça visível na tela, a função [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) retorna **false** quando chamado em uma janela nesse estado. 

Passar uma mensagem de **WM_SETREDRAW** para a função **DefWindowProc** adiciona o estilo de **WS_VISIBLE** à janela, se não estiver definido, quando *wParam* estiver definido como **true**. Se seu aplicativo enviar a mensagem de **WM_SETREDRAW** com *wParam* definido como **true** para uma janela oculta, a janela ficará visível. 

**Windows 10 e posterior; Windows Server 2016 e posterior**. O sistema define uma propriedade chamada *SysSetRedraw* em uma janela cujo procedimento de janela passa **WM_SETREDRAW** mensagens para **DefWindowProc**. Você pode usar a função [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) para obter o valor da propriedade quando ela estiver disponível. **GetProp** retorna um valor diferente de zero quando redesenhar está desabilitado. **GetProp** retornará zero quando redesenhar estiver habilitado ou quando a Propriedade Window não existir. 

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 2000 Professional \[somente aplicativos da área de trabalho\] |
| Servidor mínimo com suporte | Windows 2000 Server \[somente aplicativos da área de trabalho\] |
| Cabeçalho | <dl><dt>Winuser. h (incluir Windows. h)</dt></dl> |

## <a name="see-also"></a>Confira também

* [Visão geral de pintura e desenho](painting-and-drawing.md)
* [Pintura e desenho de mensagens](painting-and-drawing-messages.md)
* [RedrawWindow](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
