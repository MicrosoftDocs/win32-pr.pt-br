---
title: Código de notificação WM_HSCROLL (TrackBar) (WinUser. h)
description: A mensagem do WM \_ HSCROLL é enviada ao proprietário de um controle TrackBar horizontal quando o controle deslizante muda de posição. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- TrackBar (código de notificação de WM_HSCROLL) controles do Windows
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10727b745900520e8af31561236c8e93eeeb3a81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009298"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>\_Código de notificação do WM HSCROLL (TrackBar)

A mensagem do **WM \_ HSCROLL** é enviada ao proprietário de um controle TrackBar horizontal quando o controle deslizante muda de posição.

Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do controle deslizante se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) for TB \_ THUMBPOSITION ou TB \_ THUMBTRACK. Para todos os outros códigos de notificação, a palavra de ordem superior é zero; Envie a mensagem [**tbm \_ GETPOS**](tbm-getpos.md) para determinar a posição do controle deslizante.

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica um código de notificação que indica a interação do usuário com o TrackBar. Esta palavra pode ser um dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ inferior**</dt> </dl>                      | O usuário pressionou a tecla END ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**endtrack de TB \_**</dt> </dl>                | O TrackBar recebeu o [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), o que significa que o usuário lançou uma chave que enviou um código de chave virtual relevante. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB de \_ LINEDOWN**</dt> </dl>                | O usuário pressionou a tecla seta para a direita ([**VK \_ direita**](/windows/desktop/inputdev/virtual-key-codes)) ou seta para baixo ([**VK \_ down**](/windows/desktop/inputdev/virtual-key-codes)).<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**linha de TB \_**</dt> </dl>                      | O usuário pressionou a tecla seta para a esquerda ([**VK \_ esquerda**](/windows/desktop/inputdev/virtual-key-codes)) ou seta para cima ([**VK \_ cima**](/windows/desktop/inputdev/virtual-key-codes)).<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PageDown**</dt> </dl>                | O usuário clicou no canal abaixo ou à direita do controle deslizante ([**VK \_ Avançar**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB de \_ PageUp**</dt> </dl>                      | O usuário clicou no canal acima ou à esquerda do controle deslizante ([**VK \_ anterior**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB de \_ THUMBPOSITION**</dt> </dl> | O TrackBar recebeu o [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) seguindo um \_ código de notificação de THUMBTRACK TB.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB de \_ THUMBTRACK**</dt> </dl>          | O usuário arrastou o controle deslizante.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ superior**</dt> </dl>                               | O usuário pressionou a tecla HOME ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O identificador para o controle TrackBar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O código de TB \_ THUMBTRACK é normalmente usado por aplicativos que fornecem comentários quando o usuário arrasta a caixa de rolagem.

Observe que a mensagem do **WM \_ HSCROLL** transporta apenas 16 bits de dados de posição. Assim, os aplicativos que dependem exclusivamente do **WM \_ HSCROLL** (e do [**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)) para os dados da posição do controle deslizante têm um valor de posição máximo prático de 65.535.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**VSCROLL do WM \_**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

