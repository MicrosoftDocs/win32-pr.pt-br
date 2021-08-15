---
title: Como arrastar um Tree-View item
description: Este tópico demonstra o código para lidar com arrastar e soltar itens de exibição de árvore.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ee7cfc9d4fa7a6e73abd042df583ae9175de8583b050ff9621b7d2789e0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413110"
---
# <a name="how-to-drag-a-tree-view-item"></a>Como arrastar um Tree-View item

Este tópico demonstra o código para lidar com arrastar e soltar itens de exibição de árvore. O código de exemplo consiste em três funções. A primeira função inicia a operação de arrastar, a segunda função arrasta a imagem e a terceira função encerra a operação de arrastar.

> [!Note]  
> Arrastar um item de exibição de árvore normalmente envolve o processamento do código de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG),](tvn-beginrdrag.md)a mensagem [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e a mensagem [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou [**WM \_ RBUTTONUP).**](/windows/desktop/inputdev/wm-rbuttonup) Ele também envolve o uso [das funções listas](image-lists.md) de imagens para desenhar o item enquanto ele está sendo arrastado.

 

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Etapa 1: Iniciando a operação de arrastar de exibição de árvore

Um controle de exibição de árvore envia à janela pai um código de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) sempre que o usuário começa a arrastar um item. A janela pai recebe a notificação na forma de uma mensagem [**WM \_ NOTIFY**](wm-notify.md) cujo parâmetro *lParam* é o endereço de uma [**estrutura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Os membros dessa estrutura incluem as coordenadas de tela do ponteiro do mouse e uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações sobre o item a ser arrastado.

O exemplo a seguir mostra como processar a [**mensagem WM \_ NOTIFY**](wm-notify.md) para obter [TVN \_ BEGINDRAG](tvn-begindrag.md).


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



O início da operação de arrastar envolve o [**uso da função \_ ImageList BeginDrag.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) Os parâmetros da função incluem o alça para a lista de imagens que contém a imagem a ser usada durante a operação de arrastar e o índice da imagem. Você pode fornecer sua própria lista de imagens e imagem ou fazer com que o controle de exibição de árvore as crie usando a mensagem [**TVM \_ CREATEDRAGIMAGE.**](tvm-createdragimage.md)

Como a imagem de arrastar substitui o ponteiro do mouse pela duração da operação de arrastar, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) exige que você especifique um ponto quente dentro da imagem. As coordenadas do ponto de calor são relativas ao canto superior esquerdo da imagem. **ImageList \_ BeginDrag** também exige que você especifique o local inicial da imagem de arrastar. Um aplicativo normalmente define o local inicial para que o ponto quente da imagem de arrastar corresponda ao ponteiro do mouse no momento em que o usuário iniciou a operação de arrastar.

A função a seguir demonstra como começar a arrastar um item de exibição de árvore. Ele usa a imagem de arrastar fornecida pelo controle de exibição de árvore e obtém o retângulo delimitar do item para determinar o ponto apropriado para o ponto de acesso. As dimensões do retângulo delimitado são as mesmas que as da imagem.

A função captura a entrada do mouse, fazendo com que as mensagens do mouse sejam enviadas para a janela pai. A janela pai precisa das mensagens [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) subsequentes para determinar onde arrastar a imagem e a mensagem [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) para determinar quando encerrar a operação de arrastar.


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



### <a name="step-2-dragging-the-tree-view-item"></a>Etapa 2: Arrastando o item de exibição de árvore

Arraste um item de exibição de árvore chamando a função [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quando a janela pai receber uma mensagem [**WM \_ MOUSEMOVE,**](/windows/desktop/inputdev/wm-mousemove) como mostra o exemplo a seguir. O exemplo também demonstra como executar testes de acerto durante a operação de arrastar para determinar se outros itens devem ser realçados na exibição de árvore como destinos de uma operação do tipo "arrastar e soltar".


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Etapa 3: Encerrando a operação de arrastar de exibição de árvore

O exemplo a seguir mostra como encerrar uma operação de arrastar. A [**função \_ ImageList EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) é chamada quando a janela pai recebe uma [**mensagem WM \_ LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup) O alça do controle de exibição de árvore é passado para a função.


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

[Usando Tree-View controles](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um Tree-View controle](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 