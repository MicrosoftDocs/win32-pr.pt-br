---
title: Mensagem de WM_CHARTOITEM (WinUser. h)
description: Enviado por uma caixa de listagem com o \_ estilo de lbs WANTKEYBOARDINPUT para seu proprietário em resposta a uma mensagem do WM \_ Char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Controles de WM_CHARTOITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104298432"
---
# <a name="wm_chartoitem-message"></a>Mensagem do WM \_ CHARTOITEM

Enviado por uma caixa de listagem com o estilo de [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) para seu proprietário em resposta a uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o código de caractere da chave que o usuário pressionou. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do cursor.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno especifica a ação que o aplicativo realizou em resposta à mensagem. Um valor de retorno de-1 ou-2 indica que o aplicativo tratou todos os aspectos da seleção do item e não requer nenhuma ação adicional na caixa de listagem. Um valor de retorno igual a 0 ou superior especifica o índice de base zero de um item na caixa de listagem e indica que a caixa de listagem deve executar a ação padrão para o pressionamento de tecla no item especificado.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna-1.

Somente as caixas de listagem desenhadas pelo proprietário que não têm o estilo de [**lb \_ HASSTRINGS**](list-box-styles.md) podem receber essa mensagem.

Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente. O valor de *\_ MSGRESULT DWL* definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

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

[**VKEYTOITEM do WM \_**](wm-vkeytoitem.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**caractere do WM \_**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

