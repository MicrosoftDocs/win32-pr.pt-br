---
title: Mensagem de SHAREVISTRING (Commdlg. h)
description: Uma caixa de diálogo abrir ou salvar como envia a mensagem registrada SHAREVISTRING para o procedimento de gancho, OFNHookProc, se ocorrer uma violação de compartilhamento para o arquivo selecionado quando o usuário clicar no botão OK.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Caixas de diálogo de mensagem SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455567"
---
# <a name="sharevistring-message"></a>Mensagem SHAREVISTRING

\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]

Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **SHAREVISTRING** para o procedimento de gancho, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), se ocorrer uma violação de compartilhamento para o arquivo selecionado quando o usuário clicar no botão **OK** .


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . O membro **lpstrFile** dessa estrutura contém o nome do arquivo que causou a violação de compartilhamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O procedimento de gancho deve retornar um dos valores a seguir para indicar como a caixa de diálogo deve tratar a violação de compartilhamento.



| Código/valor de retorno                                                                                                                                           | Descrição                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Aceitar o nome do arquivo<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Rejeite o nome do arquivo, mas não avise o usuário. O aplicativo é responsável por exibir uma mensagem de aviso.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Rejeite o nome do arquivo e exibe uma mensagem de aviso (o mesmo resultado que se não houvesse nenhum procedimento de gancho).<br/>       |



 

## <a name="remarks"></a>Comentários

O procedimento de gancho deve especificar a constante **SHAREVISTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.

A caixa de diálogo enviará a mensagem registrada **SHAREVISTRING** somente se você não tiver especificado o sinalizador **OFN \_ SHAREAWARE** no membro **flags** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando criou a caixa de diálogo.

Se o procedimento de gancho retornar um valor indefinido, a caixa de diálogo responderá como se **OFN \_ SHAREWARN** fosse retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SHAREVISTRINGW** (Unicode) e **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SHAREVIOLATION CDN**](cdn-shareviolation.md)
</dt> <dt>

[**DA OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

