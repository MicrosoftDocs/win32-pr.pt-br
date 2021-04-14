---
title: Mensagem de FINDMSGSTRING (Commdlg. h)
description: Uma caixa de diálogo Localizar ou substituir envia a mensagem registrada FINDMSGSTRING para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão Localizar próximo, substituir ou substituir tudo ou fecha a caixa de diálogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Caixas de diálogo de mensagem FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499740"
---
# <a name="findmsgstring-message"></a>Mensagem FINDMSGSTRING

Uma caixa de diálogo **Localizar** ou **substituir** envia a mensagem registrada **FINDMSGSTRING** para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão **Localizar próximo**, **substituir** ou **substituir tudo** ou fecha a caixa de diálogo.


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) . Os membros dessa estrutura contêm a entrada de usuário mais recente, incluindo a cadeia de caracteres a ser pesquisada, a cadeia de caracteres de substituição (se houver) e as opções de pesquisa e substituição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Você deve especificar a constante **FINDMSGSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.

Ao criar a caixa de diálogo, use o membro **hwndOwner** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para identificar a janela para receber mensagens **FINDMSGSTRING** .

O membro **flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) inclui um dos sinalizadores a seguir para indicar o evento que causou a mensagem.



| Sinalizador                            | Significado                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ DIALOGTERM** (0x00000040) | A caixa de diálogo está fechando. Depois que a janela do proprietário processa essa mensagem, um identificador para a caixa de diálogo não é mais válido.                                                                                    |
| **Fr \_ LOCALIZARPRÓXIMO** (0x00000008)   | O usuário clicou no botão **Localizar próximo** em uma caixa de diálogo **Localizar** ou **substituir** . O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser pesquisada.                                                         |
| **Fr \_ REPLACE** (0x00000010)    | O usuário clicou no botão **substituir** em uma caixa de diálogo **substituir** . O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o membro **lpstrReplaceWith** especifica a cadeia de caracteres de substituição.     |
| **Fr \_ REPLACEALL** (0x00000020) | O usuário clicou no botão **substituir tudo** em uma caixa de diálogo **substituir** . O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o membro **lpstrReplaceWith** especifica a cadeia de caracteres de substituição. |



 

Para uma mensagem **Localizar próximo** ou **substituir tudo** , o membro **sinalizadores** pode incluir um ou mais dos sinalizadores a seguir para indicar as opções de pesquisa.



| Sinalizador                           | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ INOPERANTE** (0x00000001)      | Se definido, o botão **para baixo** da direção botões de opção é selecionado indicando que o usuário deseja pesquisar do local atual até o fim do documento. Se **fr \_ baixo** não estiver definido, o botão para **cima** será selecionado para que o usuário queira Pesquisar até o início do documento.       |
| **Fr \_ MATCHCASE** (0x00000004) | Se definido, a caixa de seleção **diferenciar maiúsculas de minúsculas** é marcada indicando que o usuário quer que a pesquisa diferencia maiúsculas de minúsculas. Se **fr \_ MATCHCASE** não estiver definido, a caixa de seleção será desmarcada, de modo que a pesquisa não deve diferenciar maiúsculas de minúsculas.                                                                         |
| **Fr \_ WHOLEWORD** (0x00000002) | Se definido, a caixa de seleção **corresponder somente palavra inteira** estará marcada indicando que o usuário deseja pesquisar apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa. Se **fr \_ WHOLEWORD** não for definido, a caixa de seleção será desmarcada, de modo que você também deverá Pesquisar fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FINDMSGSTRINGW** (Unicode) e **FINDMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

