---
title: Mensagem de WM_CHOOSEFONT_GETLOGFONT (Commdlg. h)
description: Um aplicativo envia a \_ \_ mensagem GETLOGFONT do WM ChooseFont para uma caixa de diálogo fonte para recuperar informações sobre as seleções de fontes atuais do usuário.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Caixas de diálogo de WM_CHOOSEFONT_GETLOGFONT mensagem
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fb429c3cd66af28485edf2979d2efbe50b3205a2142e963c8c3bb51ef5713f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280427"
---
# <a name="wm_choosefont_getlogfont-message"></a>Mensagem de GETLOGFONT do WM \_ ChooseFont \_

Um aplicativo envia a **mensagem \_ \_ GETLOGFONT do WM ChooseFont** para uma caixa de diálogo **fonte** para recuperar informações sobre as seleções de fontes atuais do usuário.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recebe informações sobre as seleções de fonte atuais do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) cria uma caixa de diálogo de **fonte** . Quando o usuário fecha a caixa de diálogo **fonte** , a função **ChooseFont** retorna informações sobre as seleções de fontes do usuário na estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . O membro **lpLogFont** da estrutura **ChooseFont** é um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

Use a **mensagem \_ \_ GETLOGFONT do WM ChooseFont** para obter informações sobre as seleções de fontes atuais do usuário enquanto a caixa de diálogo **fonte** está aberta. Por exemplo, se você habilitar o botão **aplicar** na caixa de diálogo **fonte** , envie a mensagem para obter as informações de fonte a serem aplicadas à seleção de texto atual.

Normalmente, você habilita um procedimento de gancho [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para processar mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para o botão **aplicar** . Quando o usuário clica no botão **aplicar** , o procedimento de gancho envia a mensagem **GETLOGFONT do WM \_ ChooseFont \_** para a caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

