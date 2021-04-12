---
title: Como criar barras de rolagem
description: Ao criar uma janela sobreposta, pop-up ou filho, você pode adicionar barras de rolagem padrão usando a função CreateWindowEx e especificando WS \_ HSCROLL, WS \_ VSCROLL ou ambos os estilos.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454393"
---
# <a name="how-to-create-scroll-bars"></a><span data-ttu-id="16431-103">Como criar barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="16431-103">How to Create Scroll Bars</span></span>

<span data-ttu-id="16431-104">Ao criar uma janela sobreposta, pop-up ou filho, você pode adicionar barras de rolagem padrão usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando WS \_ HSCROLL, WS \_ VSCROLL ou ambos os estilos.</span><span class="sxs-lookup"><span data-stu-id="16431-104">When creating an overlapped, pop-up, or child window, you can add standard scroll bars by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying WS\_HSCROLL, WS\_VSCROLL, or both styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="16431-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="16431-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="16431-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="16431-106">Technologies</span></span>

-   [<span data-ttu-id="16431-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="16431-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="16431-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="16431-108">Prerequisites</span></span>

-   <span data-ttu-id="16431-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="16431-109">C/C++</span></span>
-   <span data-ttu-id="16431-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="16431-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="16431-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="16431-111">Instructions</span></span>

### <a name="create-a-scroll-bar"></a><span data-ttu-id="16431-112">Criar uma barra de rolagem</span><span class="sxs-lookup"><span data-stu-id="16431-112">Create a Scroll Bar</span></span>

<span data-ttu-id="16431-113">O exemplo a seguir cria uma janela com barras de rolagem horizontal e vertical padrão.</span><span class="sxs-lookup"><span data-stu-id="16431-113">The following example creates a window with standard horizontal and vertical scroll bars.</span></span>


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



<span data-ttu-id="16431-114">Para processar mensagens da barra de rolagem para essas barras de rolagem, você deve incluir o código apropriado no procedimento da janela principal.</span><span class="sxs-lookup"><span data-stu-id="16431-114">To process scroll bar messages for these scroll bars, you must include appropriate code in the main window procedure.</span></span>

<span data-ttu-id="16431-115">Você pode usar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar uma barra de rolagem especificando a classe da janela ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="16431-115">You can use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a scroll bar by specifying the SCROLLBAR window class.</span></span> <span data-ttu-id="16431-116">Isso cria uma barra de rolagem horizontal ou vertical, dependendo se o [**SBS \_ na horizontal**](scroll-bar-control-styles.md) ou o [**SBS \_ Vert**](scroll-bar-control-styles.md) é especificado como o estilo de janela.</span><span class="sxs-lookup"><span data-stu-id="16431-116">This creates a horizontal or vertical scroll bar, depending on whether [**SBS\_HORZ**](scroll-bar-control-styles.md) or [**SBS\_VERT**](scroll-bar-control-styles.md) is specified as the window style.</span></span> <span data-ttu-id="16431-117">O tamanho da barra de rolagem e sua posição em relação à sua janela pai também podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="16431-117">The scroll bar size and its position relative to its parent window can also be specified.</span></span>

<span data-ttu-id="16431-118">O exemplo a seguir cria uma barra de rolagem horizontal posicionada ao longo da parte inferior da área do cliente da janela pai.</span><span class="sxs-lookup"><span data-stu-id="16431-118">The following example creates a horizontal scroll bar that is positioned along the bottom of the parent window's client area.</span></span>


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a><span data-ttu-id="16431-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16431-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16431-120">Usando barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="16431-120">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="16431-121">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="16431-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 