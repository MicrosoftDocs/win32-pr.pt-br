---
title: Como lidar com botões suspensos
description: Um botão suspenso pode apresentar aos usuários uma lista de opções.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103640342"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="bc59b-103">Como lidar com botões suspensos</span><span class="sxs-lookup"><span data-stu-id="bc59b-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="bc59b-104">Um botão suspenso pode apresentar aos usuários uma lista de opções.</span><span class="sxs-lookup"><span data-stu-id="bc59b-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="bc59b-105">Para criar esse estilo de botão, especifique o [**estilo \_ suspenso BTNS**](toolbar-control-and-button-styles.md) (também chamado [**de \_ lista suspensa TBSTYLE**](toolbar-control-and-button-styles.md) para compatibilidade com versões anteriores dos controles comuns).</span><span class="sxs-lookup"><span data-stu-id="bc59b-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="bc59b-106">Para mostrar um botão suspenso com uma seta, você também deve definir o estilo da barra de ferramentas [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) enviando uma mensagem de [**TB \_ Extended**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="bc59b-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="bc59b-107">A ilustração a seguir mostra um botão suspenso "abrir" com o menu de contexto aberto e mostrando uma lista de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bc59b-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="bc59b-108">Neste exemplo, a barra de ferramentas tem o estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bc59b-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![captura de tela de uma caixa de diálogo com três itens da barra de ferramentas representados por ícones; um tem uma seta suspensa expandida e um menu de contexto de três itens](images/tb-dropdown.png)

<span data-ttu-id="bc59b-110">A ilustração a seguir mostra a mesma barra de ferramentas, desta vez sem o estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bc59b-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![captura de tela de uma caixa de diálogo anterior, mas o ícone com o menu de contexto não tem uma seta suspensa](images/tb-dropdown2.png)

<span data-ttu-id="bc59b-112">Quando os usuários clicam em um botão da barra de ferramentas que usa o estilo [**\_ suspenso BTNS**](toolbar-control-and-button-styles.md) , o controle Toolbar envia à janela pai um código de notificação [ \_ DropDown tbn](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="bc59b-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bc59b-113">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="bc59b-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bc59b-114">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="bc59b-114">Technologies</span></span>

-   [<span data-ttu-id="bc59b-115">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="bc59b-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bc59b-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="bc59b-116">Prerequisites</span></span>

-   <span data-ttu-id="bc59b-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="bc59b-117">C/C++</span></span>
-   <span data-ttu-id="bc59b-118">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="bc59b-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bc59b-119">Instruções</span><span class="sxs-lookup"><span data-stu-id="bc59b-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="bc59b-120">Manipular um botão suspenso</span><span class="sxs-lookup"><span data-stu-id="bc59b-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="bc59b-121">O exemplo de código a seguir demonstra como um aplicativo pode dar suporte a um botão suspenso em um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="bc59b-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="bc59b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc59b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc59b-123">Usando controles da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="bc59b-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="bc59b-124">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bc59b-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




