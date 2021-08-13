---
title: WM_VSCROLLCLIPBOARD mensagem (Winuser.h)
description: Enviado ao proprietário da área de transferência por uma janela do visualizador da área de transferência quando a área de transferência contém dados no formato CF OWNERDISPLAY e um evento ocorre na barra de rolagem vertical do visualizador da área de \_ transferência.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD de dados de Exchange
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcf634870ce232543cd20ccd42c9e8ca255705810e81af39cc6e81f8e41658d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544871"
---
# <a name="wm_vscrollclipboard-message"></a>Mensagem WM \_ VSCROLLCLIPBOARD

Enviado ao proprietário da área de transferência por uma janela do visualizador da área de transferência quando a área de transferência contém dados no formato [**\_ CF OWNERDISPLAY**](standard-clipboard-formats.md) e um evento ocorre na barra de rolagem vertical do visualizador da área de transferência. O proprietário deve rolar a imagem da área de transferência e atualizar os valores da barra de rolagem.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela do visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa *de lParam* especifica um evento de barra de rolagem. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                         | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ INFERIOR**</dt> <dt>7</dt> </dl>                      | Role para a parte inferior direita.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Role a rolagem final.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Role uma linha para baixo.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINE-IN-TIME**</dt> <dt>0</dt> </dl>                      | Role uma linha para cima.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt> </dl>                | Role uma página para baixo.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Role uma página para cima.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Role até a posição absoluta. A posição atual é especificada pela palavra de ordem alta.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> <dt>6</dt> </dl>                               | Role para a parte superior esquerda.<br/>                                                                  |



 

A palavra de ordem alta *de lParam* especificará a posição atual da caixa de rolagem se a palavra de ordem baixa de *lParam* for **SB \_ THUMBPOSITION;** caso contrário, a palavra de ordem alta *de lParam* não será usada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

O proprietário da área de transferência pode usar a [**função ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para rolar a imagem na janela do visualizador da área de transferência e invalidar a região apropriada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitual**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

