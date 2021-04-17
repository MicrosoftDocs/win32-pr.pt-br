---
title: Mensagem de WM_CTLCOLOREDIT (WinUser. h)
description: Um controle de edição que não é somente leitura ou desabilitado envia a \_ mensagem do WM CTLCOLOREDIT para sua janela pai quando o controle está prestes a ser desenhado.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Controles de WM_CTLCOLOREDIT de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454611"
---
# <a name="wm_ctlcoloredit-message"></a>Mensagem do WM \_ CTLCOLOREDIT

Um controle de edição que não é somente leitura ou desabilitado envia a mensagem do **WM \_ CTLCOLOREDIT** para sua janela pai quando o controle está prestes a ser desenhado. Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto de dispositivo especificado para definir o texto e as cores de plano de fundo do controle de edição.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo para a janela de controle de edição.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o controle de edição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar o identificador de um pincel. O sistema usa o pincel para pintar o plano de fundo do controle de edição.

## <a name="remarks"></a>Comentários

Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel. Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle de edição.

Os controles de edição somente leitura ou desabilitados não enviam a mensagem do **WM \_ CTLCOLOREDIT** ; em vez disso, eles enviam a mensagem do [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) .

A mensagem do **WM \_ CTLCOLOREDIT** nunca é enviada entre threads, ela é enviada somente dentro do mesmo thread.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada. O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

**Edição avançada:** Não há suporte para esta mensagem. Para definir a cor do plano de fundo para um controle de edição rico, use a mensagem em [**\_ SETBKGNDCOLOR**](em-setbkgndcolor.md) .

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

[**em \_ SETBKGNDCOLOR**](em-setbkgndcolor.md)
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
</dt> </dl>

 

