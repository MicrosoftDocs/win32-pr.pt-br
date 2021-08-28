---
title: WM_XBUTTONDOWN mensagem (Winuser.h)
description: Postado quando o usuário pressiona o primeiro ou segundo botão X enquanto o cursor está na área do cliente de uma janela.
ms.assetid: 4d972841-1513-4925-9d59-2557233561a2
keywords:
- WM_XBUTTONDOWN entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_XBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a53ed8c6cfd285927ad3a0be83ce219ece8a203e0e062995c2abb1725042f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716976"
---
# <a name="wm_xbuttondown-message"></a>Mensagem WM \_ XBUTTONDOWN

Postado quando o usuário pressiona o primeiro ou segundo botão X enquanto o cursor está na área do cliente de uma janela. Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor. Caso contrário, a mensagem será postada na janela que capturou o mouse.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_XBUTTONDOWN                  0x020B
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



 

A palavra de ordem alta indica qual botão foi clicado. Pode ser um dos seguintes valores.



| Valor                                                                                                                                                                                                     | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | O primeiro botão X foi clicado.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | O segundo botão X foi clicado.<br/> |



 

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

 

Ao contrário [**das mensagens WM \_ LBUTTONDOWN,**](wm-lbuttondown.md) [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)e [**WM \_ RBUTTONDOWN,**](wm-rbuttondown.md) um aplicativo deverá retornar **TRUE** dessa mensagem se processá-lo. Isso permite que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.

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

[**Setcapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
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

 

