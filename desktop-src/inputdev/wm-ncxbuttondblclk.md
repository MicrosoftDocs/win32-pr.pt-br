---
title: Mensagem de WM_NCXBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes no primeiro ou no segundo botão X enquanto o cursor está na área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- Entrada de mouse e teclado de mensagem WM_NCXBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b5b0deb3efb84af2bdd862377411d86328ee7ef72242a6e27759b819cdab2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482636"
---
# <a name="wm_ncxbuttondblclk-message"></a>Mensagem do WM \_ NCXBUTTONDBLCLK

Postado quando o usuário clica duas vezes no primeiro ou no segundo botão X enquanto o cursor está na área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) do processamento da mensagem do [**WM \_ NCHITTEST**](wm-nchittest.md) . Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.

A palavra de ordem superior indica qual botão foi clicado duas vezes. Pode ser um dos seguintes valores.



| Valor                                                                                                                                                                                                     | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XButton1**</dt> <dt>0x0001</dt> </dl> | O primeiro botão X foi clicado duas vezes.<br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XButton2**</dt> <dt>0x0002</dt> </dl> | O segundo botão X foi clicado duas vezes.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor. As coordenadas são relativas ao canto superior esquerdo da tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar **true**. Para obter mais informações sobre como processar o valor de retorno, consulte a seção comentários.

## <a name="remarks"></a>Comentários

Use o código a seguir para obter as informações no parâmetro *wParam* .


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



Você também pode usar o código a seguir para obter as coordenadas x e y do *lParam*:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.

 

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testa o ponto especificado para obter a posição do cursor e executa a ação apropriada. Se apropriado, ele envia a [**mensagem \_ SYSCOMMAND do WM**](/windows/desktop/menurc/wm-syscommand) para a janela.

Uma janela não precisa ter o estilo **cs \_ DBLCLKS** para receber mensagens do **WM \_ NCXBUTTONDBLCLK** . O sistema gera uma mensagem do **WM \_ NCXBUTTONDBLCLK** quando o usuário pressiona, libera e novamente pressiona um botão X dentro do limite de tempo de clique duplo do sistema. Clicar duas vezes em um desses botões gera quatro mensagens: [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md), **WM \_ NCXBUTTONDBLCLK** e **WM \_ NCXBUTTONUP** novamente.

Ao contrário das mensagens do [**WM \_ NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), do [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)e do [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) , um aplicativo deve retornar **true** dessa mensagem se a processar. isso permitirá que o software que simula essa mensagem em sistemas Windows anteriores a Windows 2000 para determinar se o procedimento de janela processou a mensagem ou se chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windowsx. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTER \_ \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**NCHITTEST do WM \_**](wm-nchittest.md)
</dt> <dt>

[**NCXBUTTONDOWN do WM \_**](wm-ncxbuttondown.md)
</dt> <dt>

[**NCXBUTTONUP do WM \_**](wm-ncxbuttonup.md)
</dt> <dt>

[**SYSCOMMAND do WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**FAIXAS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

