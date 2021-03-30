---
title: Como arrastar uma imagem
description: Este tópico demonstra como arrastar uma imagem na tela. As funções de arrastar movem uma imagem suavemente, em cores e sem qualquer piscar do cursor. Imagens mascaradas e não mascaradas podem ser arrastadas.
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da495ef9ee0895c04a856f456fcda3e3125f2957
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641941"
---
# <a name="how-to-drag-an-image"></a>Como arrastar uma imagem

Este tópico demonstra como arrastar uma imagem na tela. As funções de arrastar movem uma imagem suavemente, em cores e sem qualquer piscar do cursor. Imagens mascaradas e não mascaradas podem ser arrastadas.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="step-1-begin-the-drag-operation"></a>Etapa 1: iniciar a operação de arrastar.

Use a função [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) para iniciar uma operação de arrastar.

A função definida pelo usuário no seguinte exemplo de código C++ destina-se a ser chamada em resposta a uma mensagem de botão do mouse suspensa, como o [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). A função determina se o usuário clicou dentro do retângulo delimitador da imagem. Se o usuário tiver clicado, a função capturará a entrada do mouse, apagará a imagem da área do cliente e calculará a posição do ponto de acesso dentro da imagem. A função define o ponto de acesso para coincidir com o ponto de acesso do cursor do mouse. Em seguida, a função inicia a operação de arrastar chamando [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a>Etapa 2: mover a imagem.

A função [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) move a imagem para um novo local.

A função definida pelo usuário no exemplo de código C++ a seguir destina-se a ser chamada em resposta à mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) . Ele arrasta a imagem para um novo local.


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a>Etapa 3: terminar a operação de arrastar.

A função definida pelo usuário no exemplo de código C++ a seguir chama a função [**ImageList \_ endarraste**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) para finalizar a operação de arrastar. Em seguida, ele chama a função [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) para desbloquear a janela e ocultar a imagem de arrastar, permitindo que a janela seja atualizada.


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de listas de imagens](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Sobre as listas de imagens](image-lists.md)
</dt> <dt>

[Usando listas de imagens](using-image-lists.md)
</dt> </dl>

 

 