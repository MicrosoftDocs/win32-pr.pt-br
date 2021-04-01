---
title: Como criar um controle ComboBoxEx
description: Este tópico demonstra como criar um controle ComboBoxEx.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917821"
---
# <a name="how-to-create-a-comboboxex-control"></a><span data-ttu-id="63f5e-103">Como criar um controle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="63f5e-103">How to Create a ComboBoxEx Control</span></span>

<span data-ttu-id="63f5e-104">Este tópico demonstra como criar um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="63f5e-104">This topic demonstrates how to create a ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="63f5e-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="63f5e-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="63f5e-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="63f5e-106">Technologies</span></span>

-   [<span data-ttu-id="63f5e-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="63f5e-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="63f5e-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="63f5e-108">Prerequisites</span></span>

-   <span data-ttu-id="63f5e-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="63f5e-109">C/C++</span></span>
-   <span data-ttu-id="63f5e-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="63f5e-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="63f5e-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="63f5e-111">Instructions</span></span>


<span data-ttu-id="63f5e-112">Para criar um controle ComboBoxEx, chame a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , usando [**WC \_ ComboBoxEx**](common-control-window-classes.md) como a classe de janela.</span><span class="sxs-lookup"><span data-stu-id="63f5e-112">To create a ComboBoxEx control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, using [**WC\_COMBOBOXEX**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="63f5e-113">Você deve primeiro registrar a classe de janela chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , ao especificar o \_ bit das classes USEREX ICC \_ na estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que acompanha.</span><span class="sxs-lookup"><span data-stu-id="63f5e-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, while specifying the ICC\_USEREX\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="complete-example"></a><span data-ttu-id="63f5e-114">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="63f5e-114">Complete example</span></span>

<span data-ttu-id="63f5e-115">A função definida pelo aplicativo a seguir cria um controle ComboBoxEx com o estilo [**\_ DROPDOWN do CBS**](combo-box-styles.md) na janela principal.</span><span class="sxs-lookup"><span data-stu-id="63f5e-115">The following application-defined function creates a ComboBoxEx control with the [**CBS\_DROPDOWN**](combo-box-styles.md) style in the main window.</span></span>


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a><span data-ttu-id="63f5e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63f5e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f5e-117">Sobre controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="63f5e-117">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="63f5e-118">Referência de controle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="63f5e-118">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="63f5e-119">Usando controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="63f5e-119">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="63f5e-120">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="63f5e-120">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 