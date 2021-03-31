---
title: Como criar uma dica de ferramenta para uma área retangular
description: O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635286"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="18482-103">Como criar uma dica de ferramenta para uma área retangular</span><span class="sxs-lookup"><span data-stu-id="18482-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="18482-104">O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="18482-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="18482-105">A ilustração a seguir mostra a dica de ferramenta que é exibida quando o ponteiro do mouse está dentro da janela do cliente de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="18482-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="18482-106">O identificador da caixa de diálogo foi passado para a função mostrada no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="18482-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![captura de tela de uma caixa de diálogo; o ponteiro do mouse está dentro da janela do cliente e uma dica de ferramenta é visível](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="18482-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="18482-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="18482-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="18482-109">Technologies</span></span>

-   [<span data-ttu-id="18482-110">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="18482-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="18482-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="18482-111">Prerequisites</span></span>

-   <span data-ttu-id="18482-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="18482-112">C/C++</span></span>
-   <span data-ttu-id="18482-113">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="18482-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="18482-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="18482-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="18482-115">Criar uma dica de ferramenta para uma área retangular</span><span class="sxs-lookup"><span data-stu-id="18482-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="18482-116">O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="18482-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="18482-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18482-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18482-118">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="18482-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




