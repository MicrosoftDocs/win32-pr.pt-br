---
title: Mensagem de WM_HSCROLLCLIPBOARD (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Troca de dados de mensagem WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455675"
---
# <a name="wm_hscrollclipboard-message"></a>Mensagem do WM \_ HSCROLLCLIPBOARD

Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência. Isso ocorre quando a área de transferência contém dados no formato [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) e um evento ocorre na barra de rolagem horizontal do Visualizador da área de transferência. O proprietário deve rolar a imagem da área de transferência e atualizar os valores da barra de rolagem.


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do Visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior de *lParam* especifica um evento de barra de rolagem. Esse parâmetro pode usar um dos valores a seguir. A palavra de ordem superior de *lParam* especifica a posição atual da caixa de rolagem se a palavra de ordem inferior de *lParam* for **SB \_ THUMBPOSITION**; caso contrário, a palavra de ordem superior não será usada.



| Valor                                                                                                                                                                                                                         | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ Endrolagem**</dt> <dt>8</dt> </dl>             | Finalizar rolagem.<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ ESQUERDA**</dt> <dt>6</dt> </dl>                            | Role para o canto superior esquerdo.<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ DIREITA**</dt> <dt>7</dt> </dl>                         | Role para o canto inferior direito.<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LINELEFT**</dt> <dt>0</dt> </dl>                | Rola para a esquerda em uma unidade.<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LINERIGHT**</dt> <dt>1</dt> </dl>             | Rola para a direita em uma unidade.<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PAGELEFT**</dt> <dt>2</dt> </dl>                | Rola para a esquerda pela largura da janela.<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ FIXADA**</dt> <dt>3</dt> </dl>             | Rola para a direita pela largura da janela.<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Role até a posição absoluta. A posição atual é especificada pela palavra de ordem superior.<br/> |



 

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

 

