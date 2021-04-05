---
title: Como criar uma caixa de listagem de Multiple-Selection
description: Este tópico demonstra como exibir e acessar o conteúdo de um diretório em uma caixa de listagem de seleção múltipla.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008615"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>Como criar uma caixa de listagem de Multiple-Selection

Este tópico demonstra como exibir e acessar o conteúdo de um diretório em uma caixa de listagem de seleção múltipla. Em uma caixa de listagem de seleção múltipla, o usuário pode selecionar mais de um item por vez.

O exemplo de código C++ neste tópico permite que um usuário exiba uma lista de arquivos no diretório atual, selecione um grupo de arquivos na lista e exclua-os.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


O aplicativo de listagem de diretório deve executar as seguintes tarefas relacionadas à caixa de listagem:

-   Inicialize a caixa de listagem.
-   Recupere as seleções do usuário na caixa de listagem.
-   Remova os nomes de arquivo da caixa de listagem depois que os arquivos selecionados tiverem sido excluídos.

No exemplo de código C++ a seguir, o procedimento da caixa de diálogo Inicializa a caixa de listagem de seleção múltipla (IDC \_ FileList) usando a função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para preencher a caixa de listagem com os nomes de todos os arquivos no diretório atual.

Quando o usuário seleciona um grupo de arquivos e escolhe o botão **excluir** , o procedimento da caixa de diálogo envia a mensagem [**\_ GETSELCOUNT do lb**](lb-getselcount.md) , para recuperar o número de arquivos selecionados e a mensagem [**\_ GETSELITEMS de lb**](lb-getselitems.md) , para recuperar uma matriz dos itens da caixa de listagem selecionados. Após a exclusão de um arquivo, o procedimento da caixa de diálogo remove o item correspondente da lista, enviando a mensagem de [**\_ exclusão de lb**](lb-deletestring.md) .



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
        case WM_INITDIALOG: 
 
            // Initialize the list box by filling it with files from 
            // the current directory. 
            pszCurDir = achBuffer; 
            GetCurrentDirectory(MAX_PATH, pszCurDir);
            DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
            SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
 
            return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
                return FALSE; 
    } 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de caixa de listagem](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Sobre as caixas de listagem](about-list-boxes.md)
</dt> <dt>

[Usando caixas de listagem](using-list-boxes.md)
</dt> </dl>

 

 




