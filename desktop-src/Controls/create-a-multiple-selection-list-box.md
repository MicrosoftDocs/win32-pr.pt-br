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
# <a name="how-to-create-a-multiple-selection-list-box"></a><span data-ttu-id="dbf5a-103">Como criar uma caixa de listagem de Multiple-Selection</span><span class="sxs-lookup"><span data-stu-id="dbf5a-103">How to Create a Multiple-Selection List Box</span></span>

<span data-ttu-id="dbf5a-104">Este tópico demonstra como exibir e acessar o conteúdo de um diretório em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-104">This topic demonstrates how to display and access the contents of a directory in a multiple-selection list box.</span></span> <span data-ttu-id="dbf5a-105">Em uma caixa de listagem de seleção múltipla, o usuário pode selecionar mais de um item por vez.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-105">In a multiple-selection list box, the user can select more than one item at a time.</span></span>

<span data-ttu-id="dbf5a-106">O exemplo de código C++ neste tópico permite que um usuário exiba uma lista de arquivos no diretório atual, selecione um grupo de arquivos na lista e exclua-os.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-106">The C++ code example in this topic enables a user to view a list of files in the current directory, select a group of files from the list, and delete them.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="dbf5a-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="dbf5a-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="dbf5a-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="dbf5a-108">Technologies</span></span>

-   [<span data-ttu-id="dbf5a-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="dbf5a-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="dbf5a-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="dbf5a-110">Prerequisites</span></span>

-   <span data-ttu-id="dbf5a-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="dbf5a-111">C/C++</span></span>
-   <span data-ttu-id="dbf5a-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="dbf5a-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="dbf5a-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="dbf5a-113">Instructions</span></span>


<span data-ttu-id="dbf5a-114">O aplicativo de listagem de diretório deve executar as seguintes tarefas relacionadas à caixa de listagem:</span><span class="sxs-lookup"><span data-stu-id="dbf5a-114">The directory listing application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="dbf5a-115">Inicialize a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-115">Initialize the list box.</span></span>
-   <span data-ttu-id="dbf5a-116">Recupere as seleções do usuário na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-116">Retrieve the user's selections from the list box.</span></span>
-   <span data-ttu-id="dbf5a-117">Remova os nomes de arquivo da caixa de listagem depois que os arquivos selecionados tiverem sido excluídos.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-117">Remove the file names from the list box after the selected files have been deleted.</span></span>

<span data-ttu-id="dbf5a-118">No exemplo de código C++ a seguir, o procedimento da caixa de diálogo Inicializa a caixa de listagem de seleção múltipla (IDC \_ FileList) usando a função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) para preencher a caixa de listagem com os nomes de todos os arquivos no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-118">In the following C++ code example, the dialog box procedure initializes the multiple-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span>

<span data-ttu-id="dbf5a-119">Quando o usuário seleciona um grupo de arquivos e escolhe o botão **excluir** , o procedimento da caixa de diálogo envia a mensagem [**\_ GETSELCOUNT do lb**](lb-getselcount.md) , para recuperar o número de arquivos selecionados e a mensagem [**\_ GETSELITEMS de lb**](lb-getselitems.md) , para recuperar uma matriz dos itens da caixa de listagem selecionados.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-119">When the user selects a group of files and chooses the **Delete** button, the dialog box procedure sends the [**LB\_GETSELCOUNT**](lb-getselcount.md) message, to retrieve the number of files selected, and the [**LB\_GETSELITEMS**](lb-getselitems.md) message, to retrieve an array of selected list box items.</span></span> <span data-ttu-id="dbf5a-120">Após a exclusão de um arquivo, o procedimento da caixa de diálogo remove o item correspondente da lista, enviando a mensagem de [**\_ exclusão de lb**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf5a-120">After deleting a file, the dialog procedure removes the corresponding item from the list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="dbf5a-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbf5a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf5a-122">Referência de controle de caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="dbf5a-122">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="dbf5a-123">Sobre as caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="dbf5a-123">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="dbf5a-124">Usando caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="dbf5a-124">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




