---
title: Mensagem de WM_VSCROLLCLIPBOARD (WinUser. h)
description: Enviado ao proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no \_ formato OWNERDISPLAY do CF e um evento ocorre na barra de rolagem vertical do Visualizador da área de transferência.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- Troca de dados de mensagem WM_VSCROLLCLIPBOARD
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
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455299"
---
# <a name="wm_vscrollclipboard-message"></a>Mensagem do WM \_ VSCROLLCLIPBOARD

Enviado ao proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) e um evento ocorre na barra de rolagem vertical do Visualizador da área de transferência. O proprietário deve rolar a imagem da área de transferência e atualizar os valores da barra de rolagem.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do Visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior de *lParam* especifica um evento de barra de rolagem. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                         | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ INFERIOR**</dt> <dt>7</dt> </dl>                      | Role para o canto inferior direito.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ Endrolagem**</dt> <dt>8</dt> </dl>             | Finalizar rolagem.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Rolar uma linha para baixo.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINHAr**</dt> <dt>0</dt> </dl>                      | Rolar uma linha para cima.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt> </dl>                | Rolar uma página para baixo.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Rolar uma página para cima.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Role até a posição absoluta. A posição atual é especificada pela palavra de ordem superior.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_**</dt> <dt>6</dt> principais </dl>                               | Role para o canto superior esquerdo.<br/>                                                                  |



 

A palavra de ordem superior de *lParam* especifica a posição atual da caixa de rolagem se a palavra de ordem inferior de *lParam* for **SB \_ THUMBPOSITION**; caso contrário, a palavra de ordem superior de *lParam* não será usada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O proprietário da área de transferência pode usar a função [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para rolar a imagem na janela do Visualizador da área de transferência e invalidar a região apropriada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

