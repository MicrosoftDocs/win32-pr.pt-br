---
title: WM_CHARTOITEM mensagem (Winuser.h)
description: Enviado por uma caixa de listagem com o estilo WANTKEYBOARDINPUT do LBS para seu proprietário em \_ resposta a uma mensagem WM \_ CHAR.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM controles Windows mensagem
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
ms.openlocfilehash: 4f3809ae800cfc753925e7c27d87f970ce56c10d90ace7c23e87b46f3e0067fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957525"
---
# <a name="wm_chartoitem-message"></a>Mensagem WM \_ CHARTOITEM

Enviado por uma caixa de listagem com o estilo [**\_ WANTKEYBOARDINPUT**](list-box-styles.md) do LBS para seu proprietário em resposta a uma [**mensagem WM \_ CHAR.**](/windows/desktop/inputdev/wm-char)


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o código de caractere da chave que o usuário pressionou. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do caret.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno especifica a ação que o aplicativo realizou em resposta à mensagem. Um valor de retorno de -1 ou -2 indica que o aplicativo tratou de todos os aspectos da seleção do item e não requer mais nenhuma ação pela caixa de listagem. Um valor de retorno de 0 ou superior especifica o índice baseado em zero de um item na caixa de listagem e indica que a caixa de listagem deve executar a ação padrão para o controle de teclas no item especificado.

## <a name="remarks"></a>Comentários

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna -1.

Somente caixas de listagem desenhadas pelo proprietário que não têm o estilo [**\_ HASSTRINGS do LBS**](list-box-styles.md) podem receber essa mensagem.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá lançar o valor de retorno desejado para um **BOOL** e retornar o valor diretamente. O *valor \_ MSGRESULT* do DWL definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

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

[**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

