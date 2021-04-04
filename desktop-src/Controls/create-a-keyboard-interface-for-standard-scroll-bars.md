---
title: Como criar uma interface de teclado para barras de rolagem padrão
description: Embora um controle de barra de rolagem forneça uma interface de teclado interna, uma barra de rolagem padrão não.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824009"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="4035f-103">Como criar uma interface de teclado para barras de rolagem padrão</span><span class="sxs-lookup"><span data-stu-id="4035f-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="4035f-104">Embora um controle de barra de rolagem forneça uma interface de teclado interna, uma barra de rolagem padrão não.</span><span class="sxs-lookup"><span data-stu-id="4035f-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="4035f-105">Para implementar uma interface de teclado para uma barra de rolagem padrão, um procedimento de janela deve processar a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e examinar o código de chave virtual especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4035f-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="4035f-106">Se o código de chave virtual corresponder a uma tecla de direção, o procedimento de janela enviará a si mesmo uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com a palavra de ordem inferior do parâmetro *wParam* definido como o código de solicitação da barra de rolagem apropriada.</span><span class="sxs-lookup"><span data-stu-id="4035f-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="4035f-107">Por exemplo, quando o usuário pressiona a tecla de seta para cima, o procedimento de janela recebe uma mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) com *wParam* igual a VK \_ up.</span><span class="sxs-lookup"><span data-stu-id="4035f-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="4035f-108">Em resposta, o procedimento de janela envia a si mesmo uma mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) com a palavra de ordem inferior do *wParam* definido para o código de solicitação da linha do SB \_ .</span><span class="sxs-lookup"><span data-stu-id="4035f-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4035f-109">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="4035f-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4035f-110">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="4035f-110">Technologies</span></span>

-   [<span data-ttu-id="4035f-111">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="4035f-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4035f-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4035f-112">Prerequisites</span></span>

-   <span data-ttu-id="4035f-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="4035f-113">C/C++</span></span>
-   <span data-ttu-id="4035f-114">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="4035f-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4035f-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="4035f-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="4035f-116">Criar uma interface de teclado para uma barra de rolagem padrão</span><span class="sxs-lookup"><span data-stu-id="4035f-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="4035f-117">O exemplo de código a seguir demonstra como incluir uma interface de teclado para uma barra de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="4035f-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="4035f-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4035f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4035f-119">Usando barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="4035f-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="4035f-120">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="4035f-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 