---
title: Mensagem de WM_VSCROLL (WinUser. h)
description: A mensagem do WM \_ VSCROLL é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem vertical padrão da janela.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- controles de Windows de mensagem de WM_VSCROLL
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbb87f63cb0f4801787be1f2cb23b321470b1053a58b13d0f3eea34112b1341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636706"
---
# <a name="wm_vscroll-message"></a>Mensagem do WM \_ VSCROLL

A mensagem do **WM \_ VSCROLL** é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem vertical padrão da janela. Essa mensagem também é enviada para o proprietário de um controle de barra de rolagem vertical quando ocorre um evento de rolagem no controle.

Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual da caixa de rolagem se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) for SB \_ THUMBPOSITION ou SB \_ THUMBTRACK; caso contrário, essa palavra não será usada.

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica um valor de barra de rolagem que indica a solicitação de rolagem do usuário. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**\_parte inferior da SB**</dt> </dl>                      | Rola para a direita inferior.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**\_PERrolagem SB**</dt> </dl>             | Finaliza a rolagem.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | Rola uma linha para baixo.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**linha de SB \_**</dt> </dl>                      | Rola uma linha para cima.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PageDown**</dt> </dl>                | Rola uma página para baixo.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PageUp**</dt> </dl>                      | Rola uma página para cima.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | O usuário arrastou a caixa de rolagem (Thumb) e liberou o botão do mouse. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica a posição da caixa de rolagem no final da operação de arrastar.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | O usuário está arrastando a caixa de rolagem. Essa mensagem é enviada repetidamente até que o usuário libere o botão do mouse. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica a posição para a qual a caixa de rolagem foi arrastada.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**superior da SB \_**</dt> </dl>                               | Rola para a parte superior esquerda.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Se a mensagem for enviada por um controle de barra de rolagem, esse parâmetro será o identificador para o controle da barra de rolagem. Se a mensagem for enviada por uma barra de rolagem padrão, esse parâmetro será **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O \_ código de solicitação SB THUMBTRACK é normalmente usado por aplicativos que fornecem comentários, pois o usuário arrasta a caixa de rolagem.

Se um aplicativo rolar o conteúdo da janela, ele também deverá redefinir a posição da caixa de rolagem usando a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Observe que a mensagem do **WM \_ VSCROLL** transporta apenas 16 bits de dados da posição da caixa de rolagem. Assim, os aplicativos que dependem exclusivamente do **WM \_ VSCROLL** (e do [**WM \_ HSCROLL**](wm-hscroll.md)) para os dados da posição de rolagem têm um valor de posição máximo prático de 65.535.

No entanto, como as funções [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)e [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) dão suporte a dados de posição da barra de rolagem de 32 bits, há uma maneira de burlar a barreira de 16 bits das mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do **WM \_ VSCROLL** . Consulte **GetScrollInfo** para obter uma descrição da técnica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**HSCROLL do WM \_**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (TrackBar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

