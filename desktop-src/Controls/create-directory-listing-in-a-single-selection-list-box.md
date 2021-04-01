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
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a><span data-ttu-id="d5dd5-103">Como criar uma listagem de diretório em uma caixa de listagem de seleção única</span><span class="sxs-lookup"><span data-stu-id="d5dd5-103">How to create a directory listing in a single-selection ListBox</span></span>

<span data-ttu-id="d5dd5-104">Este tópico demonstra como usar uma caixa de listagem de seleção única para exibir e acessar o conteúdo de um diretório.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-104">This topic demonstrates how to use a single-selection list box to display and access the contents of a directory.</span></span> <span data-ttu-id="d5dd5-105">A caixa de listagem de seleção única é o tipo de caixa de listagem padrão.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-105">The single-selection list box is the default list box type.</span></span> <span data-ttu-id="d5dd5-106">Um usuário só pode selecionar um item por vez em uma caixa de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-106">A user can only select one item at a time from a single-selection list box.</span></span>

<span data-ttu-id="d5dd5-107">O exemplo de código C++ neste tópico permite que um usuário exiba uma lista de arquivos no diretório atual, selecione um arquivo na lista e exclua-o.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-107">The C++ code example in this topic enables a user to view a list of files in the current directory, select a file from the list, and delete it.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d5dd5-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="d5dd5-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d5dd5-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="d5dd5-109">Technologies</span></span>

-   [<span data-ttu-id="d5dd5-110">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="d5dd5-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d5dd5-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d5dd5-111">Prerequisites</span></span>

-   <span data-ttu-id="d5dd5-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="d5dd5-112">C/C++</span></span>
-   <span data-ttu-id="d5dd5-113">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="d5dd5-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d5dd5-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="d5dd5-114">Instructions</span></span>


<span data-ttu-id="d5dd5-115">O aplicativo de listagem de diretório deve executar as seguintes tarefas relacionadas à caixa de listagem:</span><span class="sxs-lookup"><span data-stu-id="d5dd5-115">The directory listing application must perform the following list box related tasks:</span></span>

-   <span data-ttu-id="d5dd5-116">Inicialize a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-116">Initialize the list box.</span></span>
-   <span data-ttu-id="d5dd5-117">Recupere a seleção do usuário na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-117">Retrieve the user's selection from the list box.</span></span>
-   <span data-ttu-id="d5dd5-118">Remova o nome do arquivo da caixa de listagem depois que o arquivo selecionado tiver sido excluído.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-118">Remove the file name from the list box after the selected file has been deleted.</span></span>

<span data-ttu-id="d5dd5-119">No exemplo de código C++ a seguir, o procedimento da caixa de diálogo Inicializa a caixa de listagem de seleção única (IDC \_ FileList) usando a função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para preencher a caixa de listagem com os nomes de todos os arquivos no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-119">In the following C++ code example, the dialog box procedure initializes the single-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span> <span data-ttu-id="d5dd5-120">Quando o usuário seleciona um arquivo e escolhe o botão **excluir** , a função [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera o nome do arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="d5dd5-120">When the user selects a file and chooses the **Delete** button, the [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) function retrieves the name of the selected file.</span></span> <span data-ttu-id="d5dd5-121">O código exclui o arquivo usando a função [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e atualiza a caixa de listagem do diretório enviando a mensagem de [**\_ exclusão do lb**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="d5dd5-121">The code deletes the file by using the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) function and updates the directory list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="d5dd5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5dd5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5dd5-123">Referência de controle de caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="d5dd5-123">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d5dd5-124">Sobre as caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="d5dd5-124">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="d5dd5-125">Usando caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="d5dd5-125">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 