---
title: Como criar uma caixa de listagem simples
description: Este tópico demonstra como inicializar e recuperar itens de uma caixa de listagem simples.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008609"
---
# <a name="how-to-create-a-simple-list-box"></a><span data-ttu-id="70c2d-103">Como criar uma caixa de listagem simples</span><span class="sxs-lookup"><span data-stu-id="70c2d-103">How to Create a Simple List Box</span></span>

<span data-ttu-id="70c2d-104">Este tópico demonstra como inicializar e recuperar itens de uma caixa de listagem simples.</span><span class="sxs-lookup"><span data-stu-id="70c2d-104">This topic demonstrates how to initialize and retrieve items from a simple list box.</span></span>

<span data-ttu-id="70c2d-105">O exemplo de código C++ neste tópico inclui um procedimento de caixa de diálogo que preenche uma caixa de listagem com informações sobre os jogadores em uma equipe esportiva.</span><span class="sxs-lookup"><span data-stu-id="70c2d-105">The C++ code example in this topic includes a dialog box procedure that fills a list box with information about players on a sports team.</span></span> <span data-ttu-id="70c2d-106">Quando o usuário seleciona o nome de um player na lista, as informações sobre o Player são exibidas na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="70c2d-106">When the user selects the name of a player from the list, information about the player is displayed in the dialog box.</span></span> <span data-ttu-id="70c2d-107">O estilo de janela da caixa de listagem inclui [**lbs \_ Sort**](list-box-styles.md), o que resulta em uma lista classificada de itens.</span><span class="sxs-lookup"><span data-stu-id="70c2d-107">The window style for the list box includes [**LBS\_SORT**](list-box-styles.md), which results in a sorted list of items.</span></span> <span data-ttu-id="70c2d-108">A captura de tela a seguir mostra a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="70c2d-108">The following screen shot shows the dialog box.</span></span>

![captura de tela de uma caixa de diálogo contendo uma caixa de listagem rotulada, texto sobre o item da caixa de listagem selecionado e um botão OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="70c2d-110">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="70c2d-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="70c2d-111">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="70c2d-111">Technologies</span></span>

-   [<span data-ttu-id="70c2d-112">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="70c2d-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="70c2d-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="70c2d-113">Prerequisites</span></span>

-   <span data-ttu-id="70c2d-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="70c2d-114">C/C++</span></span>
-   <span data-ttu-id="70c2d-115">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="70c2d-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="70c2d-116">Instruções</span><span class="sxs-lookup"><span data-stu-id="70c2d-116">Instructions</span></span>


<span data-ttu-id="70c2d-117">O aplicativo deve executar as seguintes tarefas relacionadas à caixa de listagem:</span><span class="sxs-lookup"><span data-stu-id="70c2d-117">The application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="70c2d-118">Inicializar a caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="70c2d-118">Initialize the list box</span></span>
-   <span data-ttu-id="70c2d-119">Recuperar a seleção do usuário na caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="70c2d-119">Retrieve the user's selection from the list box</span></span>

<span data-ttu-id="70c2d-120">No exemplo de código C++ a seguir, as informações sobre os jogadores são armazenadas em uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="70c2d-120">In the following C++ code example, information about players is stored in an array of structures.</span></span> <span data-ttu-id="70c2d-121">Durante a inicialização, o procedimento da caixa de diálogo usa a mensagem de [**\_ AddString do lb**](lb-addstring.md) para adicionar os nomes dos membros da equipe à caixa de listagem (**exemplo de \_ ListBox \_ da IDC**) um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="70c2d-121">During initialization, the dialog box procedure uses the [**LB\_ADDSTRING**](lb-addstring.md) message to add the names of team members to the list box (**IDC\_LISTBOX\_EXAMPLE**) one at a time.</span></span> <span data-ttu-id="70c2d-122">Ele também usa a [**mensagem \_ SETITEMDATA de lb**](lb-setitemdata.md) para adicionar o índice de matriz do Player à caixa de listagem como dados de item.</span><span class="sxs-lookup"><span data-stu-id="70c2d-122">It also uses the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to add the array index of the player to the list box as item data.</span></span> <span data-ttu-id="70c2d-123">Posteriormente, quando o usuário seleciona um player na caixa de listagem, o procedimento da caixa de diálogo usa a mensagem [**\_ GETITEMDATA de lb**](lb-getitemdata.md) para recuperar o índice de matriz correspondente.</span><span class="sxs-lookup"><span data-stu-id="70c2d-123">Later, when the user selects a player from the list box, the dialog box procedure uses the [**LB\_GETITEMDATA**](lb-getitemdata.md) message to retrieve the corresponding array index.</span></span> <span data-ttu-id="70c2d-124">Em seguida, ele usa o índice de matriz para recuperar informações do Player da matriz.</span><span class="sxs-lookup"><span data-stu-id="70c2d-124">It then uses the array index to retrieve player information from the array.</span></span>



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="70c2d-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70c2d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70c2d-126">Referência de controle de caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="70c2d-126">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="70c2d-127">Sobre as caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="70c2d-127">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="70c2d-128">Usando caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="70c2d-128">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




