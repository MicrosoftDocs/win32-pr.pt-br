---
title: Mensagem de WM_CHOOSEFONT_SETLOGFONT (Commdlg. h)
description: Um aplicativo envia a \_ mensagem SETLOGFONT do WM ChooseFont \_ para uma caixa de diálogo fonte para definir as informações da fonte lógica atual.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Caixas de diálogo de WM_CHOOSEFONT_SETLOGFONT mensagem
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
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644920"
---
# <a name="wm_choosefont_setlogfont-message"></a>Mensagem de SETLOGFONT do WM \_ ChooseFont \_

Um aplicativo envia a **mensagem \_ \_ SETLOGFONT do WM ChooseFont** para uma caixa de diálogo **fonte** para definir as informações da fonte lógica atual.


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

Um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém informações sobre a fonte lógica atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Ao chamar a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para criar uma caixa de diálogo de **fonte** , você pode usar o membro **lpLogFont** da estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contendo valores iniciais para a caixa de diálogo. Use a **mensagem \_ \_ SETLOGFONT do WM ChooseFont** para especificar uma estrutura **LOGFONT** com valores diferentes, enquanto a caixa de diálogo **fonte** está aberta.

Normalmente, você enviaria a mensagem de **\_ \_ SETLOGFONT do WM ChooseFont** de um procedimento de gancho de [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) . O procedimento de gancho também pode enviar as mensagens do [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md) e do [**WM \_ ChooseFont \_ SetFlags**](wm-choosefont-setflags.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**GETLOGFONT do WM \_ ChooseFont \_**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**ChooseFont do WM \_ \_**](wm-choosefont-setflags.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

