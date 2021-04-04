---
title: Como criar um controle de Tree-View
description: Para criar um controle de exibição de árvore, use a função CreateWindowEx, especificando o \_ valor de TreeView WC para a classe Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084939"
---
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="2db15-103">Como criar um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="2db15-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="2db15-104">Para criar um controle de exibição de árvore, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando o valor de [**\_ TreeView WC**](common-control-window-classes.md) para a classe Window.</span><span class="sxs-lookup"><span data-stu-id="2db15-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="2db15-105">A classe de janela de exibição de árvore é registrada no espaço de endereço do aplicativo quando a DLL de controle comum é carregada.</span><span class="sxs-lookup"><span data-stu-id="2db15-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="2db15-106">Para garantir que a DLL seja carregada, use a função [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="2db15-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2db15-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="2db15-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2db15-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="2db15-108">Technologies</span></span>

-   [<span data-ttu-id="2db15-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="2db15-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2db15-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2db15-110">Prerequisites</span></span>

-   <span data-ttu-id="2db15-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="2db15-111">C/C++</span></span>
-   <span data-ttu-id="2db15-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="2db15-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2db15-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="2db15-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="2db15-114">Criar uma instância de um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="2db15-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="2db15-115">O exemplo a seguir cria um controle de exibição de árvore que é dimensionado para se ajustar à área do cliente da janela pai.</span><span class="sxs-lookup"><span data-stu-id="2db15-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="2db15-116">Ele também usa funções definidas pelo aplicativo para associar uma lista de imagens ao controle e adicionar itens ao controle.</span><span class="sxs-lookup"><span data-stu-id="2db15-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a><span data-ttu-id="2db15-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2db15-117">Remarks</span></span>

<span data-ttu-id="2db15-118">Ao criar um controle de exibição de árvore, você também pode enviá-lo para uma mensagem do [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) para definir a fonte a ser usada para o texto.</span><span class="sxs-lookup"><span data-stu-id="2db15-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="2db15-119">Você deve enviar esta mensagem antes de inserir qualquer item.</span><span class="sxs-lookup"><span data-stu-id="2db15-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="2db15-120">Por padrão, um modo de exibição de árvore usa a fonte do título do ícone.</span><span class="sxs-lookup"><span data-stu-id="2db15-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="2db15-121">Embora você possa personalizar a fonte por item usando o [desenho personalizado](custom-draw.md), o controle de exibição de árvore usa as dimensões da fonte especificada pela mensagem do **WM \_ SetFont** para determinar o espaçamento e o layout.</span><span class="sxs-lookup"><span data-stu-id="2db15-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2db15-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2db15-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db15-123">Usando controles de Tree-View</span><span class="sxs-lookup"><span data-stu-id="2db15-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="2db15-124">O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="2db15-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 