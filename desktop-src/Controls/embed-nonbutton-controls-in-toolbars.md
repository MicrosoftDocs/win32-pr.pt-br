---
title: Como inserir controles de não botão em barras de ferramentas
description: Barras de ferramentas dão suporte apenas a botões; Portanto, se seu aplicativo exigir um tipo diferente de controle, você deverá criar uma janela filho. A ilustração a seguir mostra uma barra de ferramentas com um controle de edição inserido.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103823612"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="5dad8-104">Como inserir controles de não botão em barras de ferramentas</span><span class="sxs-lookup"><span data-stu-id="5dad8-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="5dad8-105">Barras de ferramentas dão suporte apenas a botões; Portanto, se seu aplicativo exigir um tipo diferente de controle, você deverá criar uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="5dad8-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="5dad8-106">A ilustração a seguir mostra uma barra de ferramentas com um controle de edição inserido.</span><span class="sxs-lookup"><span data-stu-id="5dad8-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![captura de tela de uma caixa de diálogo com um controle de edição na barra de ferramentas, antecedendo três ícones da barra de ferramentas](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="5dad8-108">Considere o uso de [controles Rebar](rebar-controls.md) em vez de colocar controles em barras de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5dad8-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="5dad8-109">Qualquer tipo de janela pode ser colocado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5dad8-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="5dad8-110">O código de exemplo a seguir adiciona um controle de edição como um filho da janela de controle da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5dad8-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="5dad8-111">Como a barra de ferramentas é criada e, em seguida, o controle de edição foi adicionado, você deve fornecer espaço para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="5dad8-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="5dad8-112">Uma maneira de fazer isso é adicionar um separador como um espaço reservado na barra de ferramentas, definindo a largura do separador como o número de pixels que você deseja reservar.</span><span class="sxs-lookup"><span data-stu-id="5dad8-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5dad8-113">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="5dad8-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5dad8-114">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="5dad8-114">Technologies</span></span>

-   [<span data-ttu-id="5dad8-115">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="5dad8-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5dad8-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="5dad8-116">Prerequisites</span></span>

-   <span data-ttu-id="5dad8-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="5dad8-117">C/C++</span></span>
-   <span data-ttu-id="5dad8-118">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="5dad8-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5dad8-119">Instruções</span><span class="sxs-lookup"><span data-stu-id="5dad8-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="5dad8-120">Inserir um controle de não botão em uma barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="5dad8-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="5dad8-121">O trecho de código a seguir cria a barra de ferramentas na ilustração anterior.</span><span class="sxs-lookup"><span data-stu-id="5dad8-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="5dad8-122">Este exemplo codifica as dimensões da janela filho; no entanto, para criar um aplicativo mais robusto, determine o tamanho da barra de ferramentas e faça com que a janela de controle de edição caiba.</span><span class="sxs-lookup"><span data-stu-id="5dad8-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="5dad8-123">Talvez você queira que as notificações de controle de edição vá para outra janela, como o pai da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5dad8-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="5dad8-124">Para fazer isso, crie o controle de edição como um filho da janela pai da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5dad8-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="5dad8-125">Em seguida, altere o pai do controle de edição para a barra de ferramentas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5dad8-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="5dad8-126">As notificações vão para o pai original.</span><span class="sxs-lookup"><span data-stu-id="5dad8-126">Notifications go to the original parent.</span></span> <span data-ttu-id="5dad8-127">Portanto, as mensagens de controle de edição vão para o pai da barra de ferramentas, embora a janela de edição resida na janela da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5dad8-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dad8-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dad8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dad8-129">Usando controles da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="5dad8-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="5dad8-130">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="5dad8-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




