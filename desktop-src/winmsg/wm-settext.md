---
description: Define o texto de uma janela.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Mensagem de WM_SETTEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663153"
---
# <a name="wm_settext-message"></a>\_Mensagem de SETtext do WM

Define o texto de uma janela.


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que é o texto da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

O valor de retorno será **true** se o texto estiver definido. É **false** (para um controle de edição), **lb \_ ERRSPACE** (para uma caixa de listagem) ou **CB \_ ERRSPACE** (para uma caixa de combinação) se houver espaço insuficiente disponível para definir o texto no controle de edição. Será **CB \_ Err** se essa mensagem for enviada para uma caixa de combinação sem um controle de edição.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) define e exibe o texto da janela. Para um controle de edição, o texto é o conteúdo do controle de edição. Para uma caixa de combinação, o texto é o conteúdo da parte de controle de edição da caixa de combinação. Para um botão, o texto é o nome do botão. Para outras janelas, o texto é o título da janela.

Esta mensagem não altera a seleção atual na caixa de listagem de uma caixa de combinação. Um aplicativo deve usar a [**mensagem \_ SelectString do CB**](../controls/cb-selectstring.md) para selecionar o item em uma caixa de listagem que corresponda ao texto no controle de edição.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ GETtext**](wm-gettext.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**seleção do CB \_**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
