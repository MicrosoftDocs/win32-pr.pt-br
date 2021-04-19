---
title: Mensagem de FILEOKSTRING (Commdlg. h)
description: Uma caixa de diálogo abrir ou salvar como envia a mensagem registrada FILEOKSTRING para o procedimento de gancho, OFNHookProc, quando o usuário especifica um nome de arquivo e clica no botão OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Caixas de diálogo de mensagem FILEOKSTRING
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
ms.openlocfilehash: a6fddbb3460f15e1efb946b9bd17f1c85fd031a8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590783"
---
# <a name="fileokstring-message"></a>Mensagem FILEOKSTRING

\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog). Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]

Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **FILEOKSTRING** para o procedimento de gancho, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), quando o usuário especifica um nome de arquivo e clica no botão **OK** . O procedimento de gancho pode aceitar o nome do arquivo e permitir que a caixa de diálogo seja fechada ou rejeitar o nome do arquivo e forçar a caixa de diálogo a permanecer aberta.


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

Um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . O membro **lpstrFile** dessa estrutura contém a unidade, o caminho e o nome de arquivo especificados pelo usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o procedimento de gancho retornar zero, a caixa de diálogo **abrir** ou **salvar como** aceitará o nome de arquivo especificado e fechará.

Se o procedimento de gancho retornar um valor diferente de zero, a caixa de diálogo **abrir** ou **salvar como** rejeitará o nome de arquivo especificado e permanecerá aberto.

## <a name="remarks"></a>Comentários

O procedimento de gancho deve especificar a constante **FILEOKSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_FILEOK CDN**](cdn-fileok.md)
</dt> <dt>

[**DA OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

