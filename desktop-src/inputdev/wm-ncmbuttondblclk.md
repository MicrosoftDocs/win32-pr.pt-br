---
title: Mensagem de WM_NCMBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes no botão do meio do mouse enquanto o cursor está dentro da área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- Entrada de mouse e teclado de mensagem WM_NCMBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612a0a7ca0a5731691ec244df505e3d058216e2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644541"
---
# <a name="wm_ncmbuttondblclk-message"></a>Mensagem do WM \_ NCMBUTTONDBLCLK

Postado quando o usuário clica duas vezes no botão do meio do mouse enquanto o cursor está dentro da área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) . Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor. As coordenadas são relativas ao canto superior esquerdo da tela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma janela não precisa ter o estilo **cs \_ DBLCLKS** para receber mensagens do **WM \_ NCMBUTTONDBLCLK** .

O sistema gera uma mensagem do **WM \_ NCMBUTTONDBLCLK** quando o usuário pressiona, libera e novamente pressiona o botão do meio do mouse dentro do limite de tempo de clique duplo do sistema. Clicar duas vezes no botão do meio do mouse gera quatro mensagens [**: \_ WM NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md), **WM \_ NCMBUTTONDBLCLK** e **WM \_ NCMBUTTONUP** novamente.

Você também pode usar as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair os valores das coordenadas X e y do *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.

 

Se for apropriado fazer isso, o sistema enviará a mensagem [**\_ SYSCOMMAND do WM**](/windows/desktop/menurc/wm-syscommand) para a janela.

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

[**NCMBUTTONDOWN do WM \_**](wm-ncmbuttondown.md)
</dt> <dt>

[**NCMBUTTONUP do WM \_**](wm-ncmbuttonup.md)
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

 

