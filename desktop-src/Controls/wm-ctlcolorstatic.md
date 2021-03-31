---
title: Mensagem de WM_CTLCOLORSTATIC (WinUser. h)
description: Um controle estático, ou um controle de edição que é somente leitura ou desabilitado, envia a \_ mensagem do WM CTLCOLORSTATIC para sua janela pai quando o controle está prestes a ser desenhado.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Controles de WM_CTLCOLORSTATIC de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644616"
---
# <a name="wm_ctlcolorstatic-message"></a>Mensagem do WM \_ CTLCOLORSTATIC

Um controle estático, ou um controle de edição que é somente leitura ou desabilitado, envia a mensagem do **WM \_ CTLCOLORSTATIC** para sua janela pai quando o controle está prestes a ser desenhado. Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto do dispositivo especificado para definir as cores de primeiro plano do texto e do plano de fundo do controle estático.

Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o contexto do dispositivo para a janela de controle estático.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o controle estático.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, o valor de retorno será um identificador para um pincel que o sistema usa para pintar o plano de fundo do controle estático.

## <a name="remarks"></a>Comentários

Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel. Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle estático.

Você pode definir a cor do plano de fundo do texto de um controle de edição desabilitado, mas não pode definir a cor do primeiro plano do texto. O sistema sempre usa a cor \_ GRAYTEXT.

Os controles de edição que não são somente leitura ou desabilitados não enviam a mensagem do **WM \_ CTLCOLORSTATIC** ; em vez disso, eles enviam a mensagem do [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .

A mensagem do **WM \_ CTLCOLORSTATIC** nunca é enviada entre threads; ela é enviada somente dentro do mesmo thread.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada. O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="examples"></a>Exemplos

O exemplo de C++ a seguir mostra como definir as cores de primeiro e segundo plano do texto de um controle estático em resposta à mensagem **\_ CTLCOLORSTATIC do WM** . A `hbrBkgnd` variável é uma variável **HBRUSH** estática que é inicializada como NULL e armazena o pincel de plano de fundo entre chamadas para o **WM \_ CTLCOLORSTATIC**. O pincel deve ser destruído por uma chamada para a função [**ExcluirObjeto**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) quando não for mais necessário, normalmente quando a caixa de diálogo associada for destruída.


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**CTLCOLORBTN do WM \_**](wm-ctlcolorbtn.md)
</dt> <dt>

[**CTLCOLOREDIT do WM \_**](wm-ctlcoloredit.md)
</dt> <dt>

[**CTLCOLORLISTBOX do WM \_**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**CTLCOLORSCROLLBAR do WM \_**](wm-ctlcolorscrollbar.md)
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

 

