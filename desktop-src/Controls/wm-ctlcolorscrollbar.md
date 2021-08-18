---
title: WM_CTLCOLORSCROLLBAR mensagem (Winuser.h)
description: A mensagem WM CTLCOLORSCROLLBAR é enviada para a janela pai de um controle de barra de rolagem quando o \_ controle está prestes a ser desenhado.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR controles Windows mensagem
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
ms.openlocfilehash: 35dba3394c3d8fd99fef88d6fa1869ea1129d95ae8a82cc33f2935e5688871a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018554"
---
# <a name="wm_ctlcolorscrollbar-message"></a>Mensagem WM \_ CTLCOLORSCROLLBAR

A **mensagem WM \_ CTLCOLORSCROLLBAR** é enviada para a janela pai de um controle de barra de rolagem quando o controle está prestes a ser desenhado. Respondendo a essa mensagem, a janela pai pode usar o controle de contexto de exibição para definir a cor da tela de fundo do controle da barra de rolagem.

Uma janela recebe essa mensagem por meio de [*sua função WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lidar com o contexto do dispositivo para o controle da barra de rolagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a barra de rolagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar o alça para um pincel. O sistema usa o pincel para pintar a tela de fundo do controle de barra de rolagem.

## <a name="remarks"></a>Comentários

Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) o aplicativo deverá liberar o pincel. Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush),**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) o aplicativo não precisará liberar o pincel.

Por padrão, a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle da barra de rolagem.

A **mensagem WM \_ CTLCOLORSCROLLBAR** nunca é enviada entre threads; ela só é enviada dentro do mesmo thread.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá lançar o valor de retorno desejado para um **\_ PTR INT** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **FALSE,** o tratamento de mensagens padrão será executado. O valor MSGRESULT do DWL \_ definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

A **mensagem WM \_ CTLCOLORSCROLLBAR** é usada somente por controles de barra de rolagem filho. As barras de rolagem anexadas a uma janela (WS \_ SCROLL e WS \_ VSCROLL) não geram essa mensagem. Para personalizar a aparência das barras de rolagem anexadas a uma janela, use as funções da barra de rolagem simples.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Realizepalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ CTLCOLORDLG**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

