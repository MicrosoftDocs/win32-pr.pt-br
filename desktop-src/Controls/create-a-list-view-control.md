---
title: Como criar um controle de List-View
description: Este tópico demonstra como criar um controle de exibição de lista. Para criar um controle de exibição de lista, use a função CreateWindow ou CreateWindowEx e especifique a \_ classe da janela ListView do WC.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454464"
---
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="d8591-104">Como criar um controle de List-View</span><span class="sxs-lookup"><span data-stu-id="d8591-104">How to Create a List-View Control</span></span>

<span data-ttu-id="d8591-105">Este tópico demonstra como criar um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="d8591-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="d8591-106">Para criar um controle de exibição de lista, use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especifique a classe da janela [**\_ ListView do WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="d8591-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="d8591-107">Um controle de exibição de lista também pode ser criado como parte de um modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d8591-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="d8591-108">Você deve especificar [**\_ ListView WC**](common-control-window-classes.md) como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="d8591-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="d8591-109">Para usar um controle de exibição de lista como parte de um modelo de caixa de diálogo, você deve chamar [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) ou [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) antes de criar uma instância da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d8591-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d8591-110">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="d8591-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d8591-111">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="d8591-111">Technologies</span></span>

-   [<span data-ttu-id="d8591-112">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="d8591-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d8591-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d8591-113">Prerequisites</span></span>

-   <span data-ttu-id="d8591-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="d8591-114">C/C++</span></span>
-   <span data-ttu-id="d8591-115">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="d8591-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d8591-116">Instruções</span><span class="sxs-lookup"><span data-stu-id="d8591-116">Instructions</span></span>


<span data-ttu-id="d8591-117">Primeiro, registre a classe Window chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e especificando o bit de [**\_ \_ classes ListView do ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) na estrutura **InitCommonControlsEx** que acompanha.</span><span class="sxs-lookup"><span data-stu-id="d8591-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="d8591-118">Isso garante que a DLL de controles comuns seja carregada.</span><span class="sxs-lookup"><span data-stu-id="d8591-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="d8591-119">Em seguida, use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especifique a classe da janela [**\_ ListView do WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="d8591-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="d8591-120">Por padrão, um controle de exibição de lista usa a fonte do título do ícone.</span><span class="sxs-lookup"><span data-stu-id="d8591-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="d8591-121">No entanto, você pode usar uma mensagem de [**\_ fonte do WM**](/windows/desktop/winmsg/wm-setfont) para especificar a fonte a ser usada para o texto.</span><span class="sxs-lookup"><span data-stu-id="d8591-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="d8591-122">Você deve enviar esta mensagem antes de inserir qualquer item.</span><span class="sxs-lookup"><span data-stu-id="d8591-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="d8591-123">O controle usa as dimensões da fonte que é especificada pela mensagem do **WM \_ SetFont** para determinar o espaçamento e o layout.</span><span class="sxs-lookup"><span data-stu-id="d8591-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="d8591-124">Você também pode personalizar a fonte de cada item.</span><span class="sxs-lookup"><span data-stu-id="d8591-124">You can also customize the font for each item.</span></span> <span data-ttu-id="d8591-125">Para obter mais informações, consulte [desenho personalizado](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="d8591-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="d8591-126">O exemplo de código C++ a seguir cria um controle de exibição de lista no modo de exibição de relatório.</span><span class="sxs-lookup"><span data-stu-id="d8591-126">The following C++ code example creates a list-view control in report view.</span></span>


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




<span data-ttu-id="d8591-127">Normalmente, os aplicativos de exibição de lista permitem que o usuário altere de uma exibição para outra.</span><span class="sxs-lookup"><span data-stu-id="d8591-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="d8591-128">O exemplo de código C++ a seguir altera o estilo de janela do modo de exibição de lista, que, por sua vez, altera a exibição.</span><span class="sxs-lookup"><span data-stu-id="d8591-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a><span data-ttu-id="d8591-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8591-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8591-130">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="d8591-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d8591-131">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="d8591-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="d8591-132">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="d8591-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 