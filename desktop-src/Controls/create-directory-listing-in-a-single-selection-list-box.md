---
title: Criar uma listagem de diretório em uma caixa de listagem
description: Este tópico demonstra como usar uma caixa de listagem de seleção única para exibir e acessar o conteúdo de um diretório.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917787"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Como criar uma listagem de diretório em uma caixa de listagem de seleção única

Este tópico demonstra como usar uma caixa de listagem de seleção única para exibir e acessar o conteúdo de um diretório. A caixa de listagem de seleção única é o tipo de caixa de listagem padrão. Um usuário só pode selecionar um item por vez em uma caixa de listagem de seleção única.

O exemplo de código C++ neste tópico permite que um usuário exiba uma lista de arquivos no diretório atual, selecione um arquivo na lista e exclua-o.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


O aplicativo de listagem de diretório deve executar as seguintes tarefas relacionadas à caixa de listagem:

-   Inicialize a caixa de listagem.
-   Recupere a seleção do usuário na caixa de listagem.
-   Remova o nome do arquivo da caixa de listagem depois que o arquivo selecionado tiver sido excluído.

No exemplo de código C++ a seguir, o procedimento da caixa de diálogo Inicializa a caixa de listagem de seleção única (IDC \_ FileList) usando a função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para preencher a caixa de listagem com os nomes de todos os arquivos no diretório atual. Quando o usuário seleciona um arquivo e escolhe o botão **excluir** , a função [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera o nome do arquivo selecionado. O código exclui o arquivo usando a função [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e atualiza a caixa de listagem do diretório enviando a mensagem de [**\_ exclusão do lb**](lb-deletestring.md) .



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
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
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
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

 

 