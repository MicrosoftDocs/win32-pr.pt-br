---
title: Mensagem de WM_CTLCOLORSCROLLBAR (WinUser. h)
description: A mensagem do WM \_ CTLCOLORSCROLLBAR é enviada para a janela pai de um controle de barra de rolagem quando o controle está prestes a ser desenhado.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Controles de WM_CTLCOLORSCROLLBAR de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918385"
---
# <a name="wm_ctlcolorscrollbar-message"></a>Mensagem do WM \_ CTLCOLORSCROLLBAR

A mensagem do **WM \_ CTLCOLORSCROLLBAR** é enviada para a janela pai de um controle de barra de rolagem quando o controle está prestes a ser desenhado. Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto de exibição para definir a cor da tela de fundo do controle da barra de rolagem.

Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o contexto do dispositivo para o controle da barra de rolagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a barra de rolagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar o identificador para um pincel. O sistema usa o pincel para pintar o plano de fundo do controle da barra de rolagem.

## <a name="remarks"></a>Comentários

Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel. Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle da barra de rolagem.

A mensagem do **WM \_ CTLCOLORSCROLLBAR** nunca é enviada entre threads; ela é enviada somente dentro do mesmo thread.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada. O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

A mensagem do **WM \_ CTLCOLORSCROLLBAR** é usada somente por controles da barra de rolagem filho. Barras de rolagem anexadas a uma janela (WS \_ Scroll e WS \_ VSCROLL) não geram essa mensagem. Para personalizar a aparência das barras de rolagem anexadas a uma janela, use as funções da barra de rolagem simples.

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

[**CTLCOLORBTN do WM \_**](wm-ctlcolorbtn.md)
</dt> <dt>

[**CTLCOLOREDIT do WM \_**](wm-ctlcoloredit.md)
</dt> <dt>

[**CTLCOLORLISTBOX do WM \_**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**CTLCOLORSTATIC do WM \_**](wm-ctlcolorstatic.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**CTLCOLORDLG do WM \_**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

