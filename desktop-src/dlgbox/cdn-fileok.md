---
title: CDN_FILEOK de notificação (Commdlg.h)
description: Enviado por uma caixa de diálogo Abrir ou Salvar como no estilo Explorer quando o usuário especifica um nome de arquivo e clica no botão OK.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK de diálogo de código de notificação
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e32e9b4abbae65c2c29020bdab191272921ee601eebff1e7b07e0c674c783dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787416"
---
# <a name="cdn_fileok-notification-code"></a>\_CDN Código de notificação FILEOK

Enviado por uma caixa de diálogo **Abrir** ou Salvar **como** no estilo Explorer quando o usuário especifica um nome de arquivo e clica no **botão OK.**

O [*procedimento de gancho OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem WM [**\_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)

A [**estrutura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contém uma [**estrutura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cujo** membro de código indica a CDN de notificação **\_ FILEOK.**

A [**estrutura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) também contém um ponteiro para uma estrutura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cujo membro **lpstrFile** especifica o endereço do nome de arquivo selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho retornar zero, a caixa de diálogo aceitará o nome de arquivo especificado e fechará.

Para rejeitar o nome do arquivo especificado e forçar a caixa de diálogo a permanecer aberta, retorne um valor diferente de zero do procedimento de gancho e chame a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir um valor **\_ MSGRESULT** de DWL diferente de zero.

## <a name="remarks"></a>Comentários

O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o **valor OFN \_ EXPLORER.**

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

[**Getopenfilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**Getsavefilename**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**Openfilename**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**Setwindowlong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Biblioteca de caixas de diálogo comuns](common-dialog-box-library.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ NOTIFY**](../controls/wm-notify.md)
</dt> </dl>

 

