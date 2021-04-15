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
# <a name="how-to-drag-a-tree-view-item"></a>Como arrastar um item de Tree-View

Este tópico demonstra o código para a manipulação de arrastar e soltar de itens de exibição em árvore. O código de exemplo consiste em três funções. A primeira função inicia a operação de arrastar, a segunda função arrasta a imagem e a terceira função encerra a operação de arrastar.

> [!Note]  
> Arrastar um item de exibição de árvore geralmente envolve o processamento do código de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [ \_ BEGINRDRAG](tvn-beginrdrag.md)), a mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) e a mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou do [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)). Ele também envolve o uso das funções de [listas de imagens](image-lists.md) para desenhar o item à medida que ele está sendo arrastado.

 

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Etapa 1: Iniciando a operação de arrastar de exibição de árvore

Um controle de exibição de árvore envia a janela pai um código de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) sempre que o usuário começa a arrastar um item. A janela pai recebe a notificação na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) cujo parâmetro *lParam* é o endereço de uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Os membros dessa estrutura incluem as coordenadas de tela do ponteiro do mouse e uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações sobre o item a ser arrastado.

O exemplo a seguir mostra como processar a mensagem de [**\_ notificação do WM**](wm-notify.md) para obter [TVN \_ BEGINDRAG](tvn-begindrag.md).


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



Iniciar a operação de arrastar envolve o uso da função [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) . Os parâmetros da função incluem o identificador para a lista de imagens que contém a imagem a ser usada durante a operação de arrastar e o índice da imagem. Você pode fornecer sua própria lista de imagens e imagem, ou pode fazer com que o controle de exibição de árvore as crie para você usando a mensagem [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .

Como a imagem de arrastar substitui o ponteiro do mouse pela duração da operação de arrastar, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) exige que você especifique um ponto de acesso dentro da imagem. As coordenadas do ponto de acesso são relativas ao canto superior esquerdo da imagem. **ImageList \_ BeginDrag** também exige que você especifique o local inicial da imagem de arrastar. Um aplicativo normalmente define o local inicial para que o ponto de acesso da imagem de arrastar corresponda ao ponteiro do mouse no momento em que o usuário iniciou a operação de arrastar.

A função a seguir demonstra como começar a arrastar um item de exibição de árvore. Ele usa a imagem de arrastar fornecida pelo controle de exibição de árvore e Obtém o retângulo delimitador do item para determinar o ponto apropriado para a ponto de acesso. As dimensões do retângulo delimitador são as mesmas que as da imagem.

A função captura a entrada do mouse, fazendo com que as mensagens do mouse sejam enviadas para a janela pai. A janela pai precisa das mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) posteriores para determinar onde arrastar a imagem e a mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) para determinar quando terminar a operação de arrastar.


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



### <a name="step-2-dragging-the-tree-view-item"></a>Etapa 2: arrastando o item de exibição de árvore

Arraste um item de exibição de árvore chamando a função [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quando a janela pai receber uma mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) , como mostra o exemplo a seguir. O exemplo também demonstra como executar testes de clique durante a operação de arrastar para determinar se os outros itens devem ser realçados no modo de exibição de árvore como destinos de uma operação de arrastar e soltar.


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Etapa 3: finalizando a operação de arrastar da exibição de árvore

O exemplo a seguir mostra como finalizar uma operação de arrastar. A função [**ImageList \_ endarrastar**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) é chamada quando a janela pai recebe uma mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) . O identificador do controle de exibição de árvore é passado para a função.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de Tree-View](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 