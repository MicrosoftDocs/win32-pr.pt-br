---
title: Como usar fluxos
description: Você pode usar fluxos para transferir dados para dentro ou para fora de um controle de edição rico. Um fluxo é definido por uma estrutura EDITSTREAM, que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104084415"
---
# <a name="how-to-use-streams"></a>Como usar fluxos

Você pode usar fluxos para transferir dados para dentro ou para fora de um controle de edição rico. Um fluxo é definido por uma estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo.

Para ler dados em um controle de edição rico (ou seja, transmitir nos dados), use a mensagem de [**\_ fluxo**](em-streamin.md) em em. O controle chama repetidamente a função de retorno de chamada do aplicativo, que transfere uma parte dos dados para o buffer a cada vez.

Para salvar o conteúdo de um controle de edição rico (ou seja, transmitir os dados), você pode usar a mensagem em [**\_ fluxo**](em-streamout.md) em em diante. O controle grava repetidamente no buffer e, em seguida, chama a função de retorno de chamada do aplicativo. Para cada chamada, a função de chamada de retorno salva o conteúdo do buffer.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-a-stream"></a>Usar um fluxo

O exemplo de código a seguir mostra como ler um arquivo. rtf em um controle de edição rico. O identificador de arquivo é passado para a função de retorno de chamada por meio do membro **dwCookie** da estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




