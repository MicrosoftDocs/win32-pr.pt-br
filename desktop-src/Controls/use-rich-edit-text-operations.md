---
title: Como usar operações de Rich Text de edição
description: Um aplicativo pode enviar mensagens para recuperar ou localizar texto em um controle de edição rico. Você pode recuperar o texto selecionado ou um intervalo de texto especificado.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917725"
---
# <a name="how-to-use-rich-edit-text-operations"></a>Como usar operações de Rich Text de edição

Um aplicativo pode enviar mensagens para recuperar ou localizar texto em um controle de edição rico. Você pode recuperar o texto selecionado ou um intervalo de texto especificado.

Para obter o texto selecionado em um controle de edição rico, use a mensagem em [**\_ GETSELTEXT**](em-getseltext.md) . O texto é copiado para a matriz de caracteres especificada. Você deve garantir que a matriz seja grande o suficiente para manter o texto selecionado mais um caractere nulo de terminação.

Para recuperar um intervalo de texto especificado, use a mensagem em [**\_ GetTextRange**](em-gettextrange.md) . A estrutura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) usada com essa mensagem Especifica o intervalo de texto a ser recuperado e aponta para uma matriz de caracteres que recebe o texto. Novamente, o aplicativo deve garantir que a matriz seja grande o suficiente para o texto especificado, além de um caractere nulo de terminação.

Você pode pesquisar uma cadeia de caracteres em um controle de edição rico usando as mensagens em [**\_ FINDTEXTEX**](em-findtextex.md) [**\_ LocalizarTexto**](em-findtext.md) ou em, ou seus equivalentes Unicode, em [**\_ FINDTEXTW**](em-findtextw.md) e em [**\_ FINDTEXTEXW**](em-findtextexw.md). A estrutura [**LocalizarTexto**](/windows/win32/api/richedit/ns-richedit-findtexta) usada com as versões não estendidas especifica o intervalo de texto a ser pesquisado e a cadeia de caracteres a ser pesquisada. As versões estendidas usam uma estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , que especifica as mesmas informações e também recebe os pontos inicial e final do intervalo de caracteres do texto encontrado. Você também pode especificar essas opções como se a pesquisa diferencia maiúsculas de minúsculas.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-a-rich-edit-text-operation"></a>Usar uma operação Rich Text de edição

A função de exemplo a seguir localiza o texto especificado dentro do texto selecionado em um controle de edição rico que dá suporte a Unicode. Se o destino for encontrado, ele se tornará a nova seleção.


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a>Comentários

O Microsoft Rich Edit 3,0 também dá suporte à função IME (editor de método de entrada) HexToUnicode, que permite que um usuário converta entre hexadecimal e Unicode usando teclas de acesso. Para obter mais informações, consulte [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 