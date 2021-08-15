---
title: WM_CHOOSEFONT_SETLOGFONT mensagem (Commdlg.h)
description: Um aplicativo envia a mensagem WM \_ CHOOSEFONT SETLOGFONT para uma caixa de diálogo Fonte para definir as \_ informações de fonte lógica atuais.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT caixa de diálogo de mensagem
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d35c6f54679389b411417e5539382fd322c0873e6dba87fc90efb93b8be7ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503419"
---
# <a name="wm_choosefont_setlogfont-message"></a>Mensagem WM \_ CHOOSEFONT \_ SETLOGFONT

Um aplicativo envia a **mensagem WM \_ CHOOSEFONT \_ SETLOGFONT** **para** uma caixa de diálogo Fonte para definir as informações de fonte lógica atuais.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém informações sobre a fonte lógica atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Ao chamar **a** função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para criar uma caixa de diálogo Fonte, você pode usar o membro **lpLogFont** da estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém valores iniciais para a caixa de diálogo. Use a **mensagem WM \_ CHOOSEFONT \_ SETLOGFONT** para especificar uma estrutura **LOGFONT** com valores diferentes enquanto a **caixa de** diálogo Fonte está aberta.

Normalmente, você enviaria a mensagem **WM \_ CHOOSEFONT \_ SETLOGFONT** de um procedimento de gancho [**CFHookProc.**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) O procedimento de gancho também pode enviar [**as mensagens WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) e [**WM \_ CHOOSEFONT \_ SETFLAGS.**](wm-choosefont-setflags.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Cfhookproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**Choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Biblioteca de caixas de diálogo comuns](common-dialog-box-library.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

