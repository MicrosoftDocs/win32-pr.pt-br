---
title: Como arrastar um item de Tree-View
description: Este tópico demonstra o código para a manipulação de arrastar e soltar de itens de exibição em árvore.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454405"
---
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="c9c09-103">Como arrastar um item de Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9c09-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="c9c09-104">Este tópico demonstra o código para a manipulação de arrastar e soltar de itens de exibição em árvore.</span><span class="sxs-lookup"><span data-stu-id="c9c09-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="c9c09-105">O código de exemplo consiste em três funções.</span><span class="sxs-lookup"><span data-stu-id="c9c09-105">The sample code consists of three functions.</span></span> <span data-ttu-id="c9c09-106">A primeira função inicia a operação de arrastar, a segunda função arrasta a imagem e a terceira função encerra a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="c9c09-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="c9c09-107">Arrastar um item de exibição de árvore geralmente envolve o processamento do código de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [ \_ BEGINRDRAG](tvn-beginrdrag.md)), a mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) e a mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou do [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)).</span><span class="sxs-lookup"><span data-stu-id="c9c09-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="c9c09-108">Ele também envolve o uso das funções de [listas de imagens](image-lists.md) para desenhar o item à medida que ele está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="c9c09-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="c9c09-109">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="c9c09-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c9c09-110">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="c9c09-110">Technologies</span></span>

-   [<span data-ttu-id="c9c09-111">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="c9c09-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c9c09-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c9c09-112">Prerequisites</span></span>

-   <span data-ttu-id="c9c09-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="c9c09-113">C/C++</span></span>
-   <span data-ttu-id="c9c09-114">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="c9c09-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c9c09-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="c9c09-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="c9c09-116">Etapa 1: Iniciando a operação de arrastar de exibição de árvore</span><span class="sxs-lookup"><span data-stu-id="c9c09-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="c9c09-117">Um controle de exibição de árvore envia a janela pai um código de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) sempre que o usuário começa a arrastar um item.</span><span class="sxs-lookup"><span data-stu-id="c9c09-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="c9c09-118">A janela pai recebe a notificação na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) cujo parâmetro *lParam* é o endereço de uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="c9c09-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="c9c09-119">Os membros dessa estrutura incluem as coordenadas de tela do ponteiro do mouse e uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações sobre o item a ser arrastado.</span><span class="sxs-lookup"><span data-stu-id="c9c09-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="c9c09-120">O exemplo a seguir mostra como processar a mensagem de [**\_ notificação do WM**](wm-notify.md) para obter [TVN \_ BEGINDRAG](tvn-begindrag.md).</span><span class="sxs-lookup"><span data-stu-id="c9c09-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



<span data-ttu-id="c9c09-121">Iniciar a operação de arrastar envolve o uso da função [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .</span><span class="sxs-lookup"><span data-stu-id="c9c09-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="c9c09-122">Os parâmetros da função incluem o identificador para a lista de imagens que contém a imagem a ser usada durante a operação de arrastar e o índice da imagem.</span><span class="sxs-lookup"><span data-stu-id="c9c09-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="c9c09-123">Você pode fornecer sua própria lista de imagens e imagem, ou pode fazer com que o controle de exibição de árvore as crie para você usando a mensagem [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c09-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="c9c09-124">Como a imagem de arrastar substitui o ponteiro do mouse pela duração da operação de arrastar, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) exige que você especifique um ponto de acesso dentro da imagem.</span><span class="sxs-lookup"><span data-stu-id="c9c09-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="c9c09-125">As coordenadas do ponto de acesso são relativas ao canto superior esquerdo da imagem.</span><span class="sxs-lookup"><span data-stu-id="c9c09-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="c9c09-126">**ImageList \_ BeginDrag** também exige que você especifique o local inicial da imagem de arrastar.</span><span class="sxs-lookup"><span data-stu-id="c9c09-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="c9c09-127">Um aplicativo normalmente define o local inicial para que o ponto de acesso da imagem de arrastar corresponda ao ponteiro do mouse no momento em que o usuário iniciou a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="c9c09-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="c9c09-128">A função a seguir demonstra como começar a arrastar um item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="c9c09-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="c9c09-129">Ele usa a imagem de arrastar fornecida pelo controle de exibição de árvore e Obtém o retângulo delimitador do item para determinar o ponto apropriado para a ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="c9c09-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="c9c09-130">As dimensões do retângulo delimitador são as mesmas que as da imagem.</span><span class="sxs-lookup"><span data-stu-id="c9c09-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="c9c09-131">A função captura a entrada do mouse, fazendo com que as mensagens do mouse sejam enviadas para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="c9c09-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="c9c09-132">A janela pai precisa das mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) posteriores para determinar onde arrastar a imagem e a mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) para determinar quando terminar a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="c9c09-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="c9c09-133">Etapa 2: arrastando o item de exibição de árvore</span><span class="sxs-lookup"><span data-stu-id="c9c09-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="c9c09-134">Arraste um item de exibição de árvore chamando a função [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quando a janela pai receber uma mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) , como mostra o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9c09-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="c9c09-135">O exemplo também demonstra como executar testes de clique durante a operação de arrastar para determinar se os outros itens devem ser realçados no modo de exibição de árvore como destinos de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="c9c09-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="c9c09-136">Etapa 3: finalizando a operação de arrastar da exibição de árvore</span><span class="sxs-lookup"><span data-stu-id="c9c09-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="c9c09-137">O exemplo a seguir mostra como finalizar uma operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="c9c09-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="c9c09-138">A função [**ImageList \_ endarrastar**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) é chamada quando a janela pai recebe uma mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="c9c09-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="c9c09-139">O identificador do controle de exibição de árvore é passado para a função.</span><span class="sxs-lookup"><span data-stu-id="c9c09-139">The handle of the tree-view control is passed to the function.</span></span>


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="c9c09-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9c09-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9c09-141">Usando controles de Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9c09-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="c9c09-142">O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9c09-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 