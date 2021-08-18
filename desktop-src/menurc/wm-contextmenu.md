---
title: WM_CONTEXTMENU mensagem (Winuser.h)
description: Notifica uma janela de que o usuário clicou no botão direito do mouse (clicado com o botão direito do mouse) na janela.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU menus de mensagem e outros recursos
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c036bf0711f208bae25657d572102a7f4d82525076ee1d0b6f4ebd6598e8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472501"
---
# <a name="wm_contextmenu-message"></a>Mensagem WM \_ CONTEXTMENU

Notifica uma janela de que o usuário deseja que um menu de contexto seja exibido.  O usuário pode ter clicado no botão direito do mouse (clicado com o botão direito do mouse) na janela, pressionado Shift+F10 ou pressionado a tecla applications (tecla de menu de contexto) disponível em alguns teclados.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela na qual o usuário clicou com o botão direito do mouse. Essa pode ser uma janela filho da janela que recebe a mensagem. Para obter mais informações sobre como processar essa mensagem, consulte a seção Comentários.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica a posição horizontal do cursor, em coordenadas de tela, no momento do clique do mouse.

A palavra de ordem alta especifica a posição vertical do cursor, em coordenadas de tela, no momento do clique do mouse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Uma janela pode processar essa mensagem exibindo um menu de atalho usando as funções [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) ou [**TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Para obter as posições horizontais e verticais, use o código a seguir.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Se uma janela não exibir um menu de atalho, ela deverá passar essa mensagem para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Se uma janela for uma janela filho, **DefWindowProc** enviará a mensagem ao pai. Caso contrário, **DefWindowProc** exibirá um menu de atalho padrão se a posição especificada estiver na legenda da janela.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gera a mensagem **WM \_ CONTEXTMENU** quando processa a mensagem [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) ou quando o usuário digita SHIFT+F10. A **mensagem WM \_ CONTEXTMENU** também é gerada quando o usuário pressiona e libera a [**chave aplicativos da VK. \_**](/windows/desktop/inputdev/virtual-key-codes)

Se o menu de contexto for gerado do teclado, por exemplo, se o usuário digita SHIFT+F10, as coordenadas x e y serão -1 e o aplicativo deverá exibir o menu de contexto no local da seleção atual em vez de em (xPos, yPos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Trackpopupmenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**Trackpopupmenuex**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

