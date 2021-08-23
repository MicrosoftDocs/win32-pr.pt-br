---
title: Mensagem FILEOKSTRING (Commdlg.h)
description: Uma caixa de diálogo Abrir ou Salvar como envia a mensagem registrada FILEOKSTRING para o procedimento de gancho, OFNHookProc, quando o usuário especifica um nome de arquivo e clica no botão OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Caixas de diálogo da mensagem FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942fcf03d97c7d787231e896199bce0d4c53cf78d16f6b25741e604238bf06b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741756"
---
# <a name="fileokstring-message"></a>Mensagem FILEOKSTRING

\[Começando com Windows Vista,  as  caixas de diálogo Abrir e Salvar como comuns foram superadas pela caixa [de diálogo Item Comum](../shell/common-file-dialog.md). Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]

Uma **caixa** de diálogo Abrir ou Salvar **como** envia a mensagem registrada **FILEOKSTRING** para o procedimento de [*gancho, OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)quando o usuário especifica um nome de arquivo e clica no **botão OK.** O procedimento de gancho pode aceitar o nome do arquivo e permitir que a caixa de diálogo feche ou rejeite o nome do arquivo e force a caixa de diálogo a permanecer aberta.


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) O **membro lpstrFile** dessa estrutura contém a unidade, o caminho e o nome do arquivo especificados pelo usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho retornar zero, a caixa de diálogo **Abrir** ou Salvar **como** aceitará o nome de arquivo especificado e fechará.

Se o procedimento de gancho retornar  um valor diferente de zero, a caixa de diálogo Abrir ou Salvar **como** rejeitará o nome de arquivo especificado e permanecerá aberta.

## <a name="remarks"></a>Comentários

O procedimento de gancho deve especificar a constante **FILEOKSTRING** em uma chamada para a [**função RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_CDN Fileok**](cdn-fileok.md)
</dt> <dt>

[**Openfilename**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**Registerwindowmessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Biblioteca de caixas de diálogo comuns](common-dialog-box-library.md)
</dt> </dl>

