---
title: Mensagem de WM_VKEYTOITEM (WinUser. h)
description: Enviado por uma caixa de listagem com o \_ estilo de lbs WANTKEYBOARDINPUT para seu proprietário em resposta a uma mensagem do WM \_ KEYDOWN.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Controles de WM_VKEYTOITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104297995"
---
# <a name="wm_vkeytoitem-message"></a>Mensagem do WM \_ VKEYTOITEM

Enviado por uma caixa de listagem com o estilo de [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) para seu proprietário em resposta a uma mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) .


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o código de chave virtual da chave que o usuário pressionou. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do cursor.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno especifica a ação que o aplicativo realizou em resposta à mensagem. Um valor de retorno de-2 indica que o aplicativo tratou todos os aspectos da seleção do item e não requer nenhuma ação adicional na caixa de listagem. (Consulte comentários.) Um valor de retorno de-1 indica que a caixa de listagem deve executar a ação padrão em resposta ao pressionamento de tecla. Um valor de retorno 0 ou maior especifica o índice de um item na caixa de listagem e indica que a caixa de listagem deve executar a ação padrão para o pressionamento de tecla no item especificado.

## <a name="remarks"></a>Comentários

Um valor de retorno de-2 é válido somente para chaves que não são convertidas em caracteres pelo controle de caixa de listagem. Se a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) estiver convertida em uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) e o aplicativo processar a mensagem do **WM \_ VKEYTOITEM** gerada como resultado do pressionamento da tecla, a caixa de listagem ignorará o valor de retorno e fará o processamento padrão para esse caractere). **WM \_** As mensagens de KEYDOWN geradas por chaves como VK \_ up, VK \_ down, VK \_ Next e VK \_ Previous não são convertidas em mensagens do **WM \_ Char** . Nesses casos, o trapping da mensagem **\_ VKEYTOITEM do WM** e o retorno de-2 impede que a caixa de listagem faça o processamento padrão para essa chave.

Para ajustar as chaves que geram uma mensagem char e executar processamento especial, o aplicativo deve criar uma subclasse da caixa de listagem, interceptar as mensagens de [**\_ caracteres**](/windows/desktop/inputdev/wm-char) do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e do WM e processar as mensagens adequadamente no procedimento de subclasse.

Os comentários anteriores se aplicam a caixas de listagem normais que são criadas com o estilo [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) . Se a caixa de listagem for desenhada pelo proprietário, o aplicativo deverá processar a mensagem do [**WM \_ CHARTOITEM**](wm-chartoitem.md) .

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna-1.

Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente. O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

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

[**CHARTOITEM do WM \_**](wm-chartoitem.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

