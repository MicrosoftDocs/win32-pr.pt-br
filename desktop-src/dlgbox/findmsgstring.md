---
title: Mensagem FINDMSGSTRING (Commdlg.h)
description: Uma caixa de diálogo Encontrar ou Substituir envia a mensagem registrada FINDMSGSTRING para o procedimento de janela de sua janela de proprietário quando o usuário clica no botão Encontrar Próximo, Substituir ou Substituir Tudo ou fecha a caixa de diálogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Caixas de diálogo da mensagem FINDMSGSTRING
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
ms.openlocfilehash: 5df829d09ffbb414bdf145495389d8d14db129d1c0eec2929ac0f7e1f97816f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606346"
---
# <a name="findmsgstring-message"></a>Mensagem FINDMSGSTRING

Uma **caixa** de diálogo Encontrar ou Substituir envia a mensagem registrada **FINDMSGSTRING** para o procedimento de  janela de sua janela de proprietário quando o usuário clica no botão Encontrar Próximo **,** Substituir ou Substituir Tudo ou fecha a caixa de diálogo. 


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

Um ponteiro para uma [**estrutura FINDREPLACE.**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) Os membros dessa estrutura contêm a entrada mais recente do usuário, incluindo a cadeia de caracteres a ser pesquisada, a cadeia de caracteres de substituição (se alguma) e as opções de pesquisa e substituição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Você deve especificar a **constante FINDMSGSTRING** em uma chamada para a [**função RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.

Ao criar a caixa de diálogo, use o membro **hwndOwner** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para identificar a janela para receber **mensagens FINDMSGSTRING.**

O **membro Flags** da [**estrutura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) inclui um dos sinalizadores a seguir para indicar o evento que causou a mensagem.



| Sinalizador                            | Significado                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** (0x00000040) | A caixa de diálogo está sendo fechada. Depois que a janela do proprietário processa essa mensagem, um alça para a caixa de diálogo não é mais válido.                                                                                    |
| **FR \_ FINDNEXT** (0x00000008)   | O usuário clicou no **botão Encontrar Próximo** em uma caixa de **diálogo** Encontrar **ou** Substituir. O **membro lpstrFindWhat** especifica a cadeia de caracteres a ser pesquisada.                                                         |
| **FR \_ REPLACE** (0x00000010)    | O usuário clicou no **botão Substituir** em uma **caixa de diálogo** Substituir. O **membro lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o **membro lpstrReplaceWith** especifica a cadeia de caracteres de substituição.     |
| **FR \_ REPLACEALL** (0x00000020) | O usuário clicou no **botão Substituir Tudo** em uma caixa de **diálogo** Substituir. O **membro lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o **membro lpstrReplaceWith** especifica a cadeia de caracteres de substituição. |



 

Para uma **mensagem Encontrar Próximo** ou Substituir **Tudo,** o membro **Sinalizadores** pode incluir um ou mais dos sinalizadores a seguir para indicar as opções de pesquisa.



| Sinalizador                           | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DOWN** (0x00000001)      | Se definido, o **botão Para** baixo dos botões de opção de direção é selecionado, indicando que o usuário deseja pesquisar do local atual até o final do documento. Se **FR \_ DOWN** não estiver definido, o **botão Para** cima será selecionado para que o usuário queira pesquisar até o início do documento.       |
| **FR \_ MATCHCASE** (0x00000004) | Se definido, a **caixa de seleção** Caso de Corresponder será marcada indicando que o usuário deseja que a pesquisa seja sensível a minúsculas. Se **FR \_ MATCHCASE não** estiver definido, a caixa de seleção será deseleitada, portanto, a pesquisa não deve ser sensível a maiúsculas e minúsculas.                                                                         |
| **FR \_ WHOLEWORD** (0x00000002) | Se definido, **a** caixa de seleção Corresponder Somente Palavra Inteira será marcada, indicando que o usuário deseja pesquisar apenas palavras inteiras que corresponderem à cadeia de caracteres de pesquisa. Se **FR \_ WHOLEWORD** não estiver definido, a caixa de seleção será deseleitada, portanto, você também deverá pesquisar fragmentos de palavras que corresponderem à cadeia de caracteres de pesquisa. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FINDMSGSTRINGW** (Unicode) e **FINDMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Findreplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**Registerwindowmessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Biblioteca de caixas de diálogo comuns](common-dialog-box-library.md)
</dt> </dl>

 

