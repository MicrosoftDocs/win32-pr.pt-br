---
title: WM_XBUTTONDBLCLK mensagem (Winuser.h)
description: Postado quando o usuário clica duas vezes no primeiro ou segundo botão X enquanto o cursor está na área do cliente de uma janela.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- WM_XBUTTONDBLCLK entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f15ed64871cee3b5a97ad8067e883d7ad31206896f6b20150acdb490a2f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757145"
---
# <a name="wm_xbuttondblclk-message"></a>Mensagem WM \_ XBUTTONDBLCLK

Postado quando o usuário clica duas vezes no primeiro ou segundo botão X enquanto o cursor está na área do cliente de uma janela. Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor. Caso contrário, a mensagem será postada na janela que capturou o mouse.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem baixa indica se várias chaves virtuais estão inotivas. Pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROLE**</dt> <dt>0x0008</dt> </dl>    | A tecla CTRL está inocizada.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | O botão esquerdo do mouse está ino mouse.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | O botão do meio do mouse está ino mouse.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | O botão direito do mouse está ino mouse.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | A tecla SHIFT está inobada.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | O primeiro botão X está ino mouse.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | O segundo botão X está ino mouse.<br/>     |



 

A palavra de ordem alta indica qual botão foi clicado duas vezes. Pode ser um dos seguintes valores.



| Valor                                                                                                                                                                                                     | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | O primeiro botão X foi clicado duas vezes.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | O segundo botão X foi clicado duas vezes.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica a coordenada X do cursor. A coordenada é relativa ao canto superior esquerdo da área do cliente.

A palavra de ordem alta especifica a coordenada y do cursor. A coordenada é relativa ao canto superior esquerdo da área do cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar **TRUE.** Para obter mais informações sobre como processar o valor de retorno, consulte a seção Comentários.

## <a name="remarks"></a>Comentários

Use o código a seguir para obter as informações no *parâmetro wParam:*


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



Use o código a seguir para obter a posição horizontal e vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Conforme mencionado acima, a coordenada x está na ordem baixa **a menos** que o valor de retorno; a coordenada y está em ordem alta  curta **(ambos** representam valores assinados porque podem receber valores negativos em sistemas com vários monitores). Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura [**POINTS**](/previous-versions//dd162808(v=vs.85)) do valor de retorno. Você também pode usar a [**macro GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou y.

> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor porque essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas, e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades sem sinal.

 

Somente as janelas que têm o estilo **\_ DBLCLKS CS** podem receber mensagens **WM \_ XBUTTONDBLCLK,** que o sistema gera sempre que o usuário pressiona, libera e pressiona novamente um botão X dentro do limite de tempo de clique duplo do sistema. Clicar duas vezes em um desses botões gera quatro mensagens: [**WM \_ XBUTTONDOWN,**](wm-xbuttondown.md) [**WM \_ XBUTTONUP,**](wm-xbuttonup.md) **WM \_ XBUTTONDBLCLK** e **WM \_ XBUTTONUP** novamente.

Ao contrário [**das mensagens WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)e [**WM \_ RBUTTONDBLCLK,**](wm-rbuttondblclk.md) um aplicativo deverá retornar **TRUE** dessa mensagem se processá-la. Isso permitirá que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (inclua Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ XBUTTON \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Pontos**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

