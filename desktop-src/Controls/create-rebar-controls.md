---
title: Como criar controles Rebar
description: Um aplicativo cria um controle rebar chamando a função CreateWindowEx, especificando REBARCLASSNAME como a classe Window.
ms.assetid: F17CC2A4-BDC6-48A6-9AF5-19FCF65CC39A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b38cd49e8e6016dafad5ec07c77be570a5a430
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641885"
---
# <a name="how-to-create-rebar-controls"></a><span data-ttu-id="ef4a3-103">Como criar controles Rebar</span><span class="sxs-lookup"><span data-stu-id="ef4a3-103">How to Create Rebar Controls</span></span>

<span data-ttu-id="ef4a3-104">Um aplicativo cria um controle rebar chamando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando [**REBARCLASSNAME**](common-control-window-classes.md) como a classe Window.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-104">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="ef4a3-105">O aplicativo deve primeiro registrar a classe de janela chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando o \_ bit de classes legais ICC \_ na estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-105">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ef4a3-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="ef4a3-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ef4a3-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="ef4a3-107">Technologies</span></span>

-   [<span data-ttu-id="ef4a3-108">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="ef4a3-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ef4a3-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ef4a3-109">Prerequisites</span></span>

-   <span data-ttu-id="ef4a3-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="ef4a3-110">C/C++</span></span>
-   <span data-ttu-id="ef4a3-111">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="ef4a3-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ef4a3-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="ef4a3-112">Instructions</span></span>

### <a name="create-a-rebar-control"></a><span data-ttu-id="ef4a3-113">Criar um controle rebar</span><span class="sxs-lookup"><span data-stu-id="ef4a3-113">Create a Rebar Control</span></span>

<span data-ttu-id="ef4a3-114">O exemplo a seguir cria um controle rebar com duas bandas — uma que contém uma caixa de combinação e outra que contém uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-114">The following example creates a rebar control with two bands—one that contains a combo box, and another one that contains a toolbar.</span></span> <span data-ttu-id="ef4a3-115">(Consulte a ilustração em [sobre controles Rebar](rebar-controls.md).) Esses controles são criados separadamente e são passados para a função de exemplo como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-115">(See the illustration in [About Rebar Controls](rebar-controls.md).) These controls are created separately, and are passed to the example function as parameters.</span></span>


```C++
#define NUMBUTTONS 3

HWND CreateRebar(HWND hwndOwner, HWND hwndToolbar, HWND hwndCombo)
{
    // Check parameters.
    if ((hwndToolbar == NULL) || (hwndCombo == NULL))
    {
        return NULL;
    }

    // Initialize common controls.
    INITCOMMONCONTROLSEX icex;
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC   = ICC_COOL_CLASSES | ICC_BAR_CLASSES;
    InitCommonControlsEx(&icex);

    // Create the rebar.
    HWND hwndRebar = CreateWindowEx(WS_EX_TOOLWINDOW,
        REBARCLASSNAME,
        NULL,
        WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |
        WS_CLIPCHILDREN | RBS_VARHEIGHT |
        CCS_NODIVIDER | RBS_BANDBORDERS,
        0,0,0,0,
        hwndOwner,
        NULL,
        g_hInst, // global instance handle
        NULL);

    if(!hwndRebar)
    {
        return NULL;
    }

    // Initialize band info used by both bands.
    REBARBANDINFO rbBand = { sizeof(REBARBANDINFO) };
    rbBand.fMask  = 
          RBBIM_STYLE       // fStyle is valid.
        | RBBIM_TEXT        // lpText is valid.
        | RBBIM_CHILD       // hwndChild is valid.
        | RBBIM_CHILDSIZE   // child size members are valid.
        | RBBIM_SIZE;       // cx is valid
    rbBand.fStyle = RBBS_CHILDEDGE | RBBS_GRIPPERALWAYS;  

    // Get the height of the toolbar.
    DWORD dwBtnSize = (DWORD)SendMessage(hwndToolbar, TB_GETBUTTONSIZE, 0,0);

    // Set values unique to the band with the toolbar.
    rbBand.lpText = TEXT("");
    rbBand.hwndChild = hwndToolbar;
    rbBand.cyChild = LOWORD(dwBtnSize);
    rbBand.cxMinChild = NUMBUTTONS * HIWORD(dwBtnSize);
    rbBand.cyMinChild = LOWORD(dwBtnSize);
    // The default width is the width of the buttons.
    rbBand.cx = 0;

    // Add the band that has the toolbar.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);

    // Set values unique to the band with the combo box.
    RECT rc;
    GetWindowRect(hwndCombo, &rc);
    rbBand.lpText = TEXT("Font");
    rbBand.hwndChild = hwndCombo;
    rbBand.cxMinChild = 0;
    rbBand.cyMinChild = rc.bottom - rc.top;
    // The default width should be set to some value wider than the text. The combo 
    // box itself will expand to fill the band.
    rbBand.cx = 100;

    // Add the band that has the combo box.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);
    
    return (hwndRebar);
}
```



## <a name="related-topics"></a><span data-ttu-id="ef4a3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef4a3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef4a3-117">Usando controles Rebar</span><span class="sxs-lookup"><span data-stu-id="ef4a3-117">Using Rebar Controls</span></span>](using-rebar-controls.md)
</dt> <dt>

[<span data-ttu-id="ef4a3-118">Sobre controles de rebar</span><span class="sxs-lookup"><span data-stu-id="ef4a3-118">About Rebar Controls</span></span>](rebar-controls.md)
</dt> <dt>

<span data-ttu-id="ef4a3-119">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ef4a3-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 