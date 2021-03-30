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
# <a name="how-to-drag-an-image"></a><span data-ttu-id="e63d7-105">Como arrastar uma imagem</span><span class="sxs-lookup"><span data-stu-id="e63d7-105">How to Drag an Image</span></span>

<span data-ttu-id="e63d7-106">Este tópico demonstra como arrastar uma imagem na tela.</span><span class="sxs-lookup"><span data-stu-id="e63d7-106">This topic demonstrates how to drag an image on the screen.</span></span> <span data-ttu-id="e63d7-107">As funções de arrastar movem uma imagem suavemente, em cores e sem qualquer piscar do cursor.</span><span class="sxs-lookup"><span data-stu-id="e63d7-107">The dragging functions move an image smoothly, in color, and without any flashing of the cursor.</span></span> <span data-ttu-id="e63d7-108">Imagens mascaradas e não mascaradas podem ser arrastadas.</span><span class="sxs-lookup"><span data-stu-id="e63d7-108">Both masked and unmasked images can be dragged.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e63d7-109">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="e63d7-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e63d7-110">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="e63d7-110">Technologies</span></span>

-   [<span data-ttu-id="e63d7-111">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="e63d7-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e63d7-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e63d7-112">Prerequisites</span></span>

-   <span data-ttu-id="e63d7-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="e63d7-113">C/C++</span></span>
-   <span data-ttu-id="e63d7-114">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="e63d7-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e63d7-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="e63d7-115">Instructions</span></span>

### <a name="step-1-begin-the-drag-operation"></a><span data-ttu-id="e63d7-116">Etapa 1: iniciar a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="e63d7-116">Step 1: Begin the drag operation.</span></span>

<span data-ttu-id="e63d7-117">Use a função [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) para iniciar uma operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="e63d7-117">Use the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function to begin a drag operation.</span></span>

<span data-ttu-id="e63d7-118">A função definida pelo usuário no seguinte exemplo de código C++ destina-se a ser chamada em resposta a uma mensagem de botão do mouse suspensa, como o [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="e63d7-118">The user-defined function in the following C++ code example is intended to be called in response to a mouse button-down message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="e63d7-119">A função determina se o usuário clicou dentro do retângulo delimitador da imagem.</span><span class="sxs-lookup"><span data-stu-id="e63d7-119">The function determines whether the user has clicked within the bounding rectangle of the image.</span></span> <span data-ttu-id="e63d7-120">Se o usuário tiver clicado, a função capturará a entrada do mouse, apagará a imagem da área do cliente e calculará a posição do ponto de acesso dentro da imagem.</span><span class="sxs-lookup"><span data-stu-id="e63d7-120">If the user has clicked, the function captures the mouse input, erases the image from the client area, and calculates the position for the hot spot within the image.</span></span> <span data-ttu-id="e63d7-121">A função define o ponto de acesso para coincidir com o ponto de acesso do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="e63d7-121">The function sets the hot spot to coincide with the hot spot of the mouse cursor.</span></span> <span data-ttu-id="e63d7-122">Em seguida, a função inicia a operação de arrastar chamando [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span><span class="sxs-lookup"><span data-stu-id="e63d7-122">Then the function begins the drag operation by calling [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span></span>


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



### <a name="step-2-move-the-image"></a><span data-ttu-id="e63d7-123">Etapa 2: mover a imagem.</span><span class="sxs-lookup"><span data-stu-id="e63d7-123">Step 2: Move the image.</span></span>

<span data-ttu-id="e63d7-124">A função [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) move a imagem para um novo local.</span><span class="sxs-lookup"><span data-stu-id="e63d7-124">The [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function moves the image to a new location.</span></span>

<span data-ttu-id="e63d7-125">A função definida pelo usuário no exemplo de código C++ a seguir destina-se a ser chamada em resposta à mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="e63d7-125">The user-defined function in the following C++ code example is intended to be called in response to the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="e63d7-126">Ele arrasta a imagem para um novo local.</span><span class="sxs-lookup"><span data-stu-id="e63d7-126">It drags the image to a new location.</span></span>


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



### <a name="step-3-end-the-drag-operation"></a><span data-ttu-id="e63d7-127">Etapa 3: terminar a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="e63d7-127">Step 3: End the drag operation.</span></span>

<span data-ttu-id="e63d7-128">A função definida pelo usuário no exemplo de código C++ a seguir chama a função [**ImageList \_ endarraste**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) para finalizar a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="e63d7-128">The user-defined function in the following C++ code example calls the [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function to end the drag operation.</span></span> <span data-ttu-id="e63d7-129">Em seguida, ele chama a função [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) para desbloquear a janela e ocultar a imagem de arrastar, permitindo que a janela seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="e63d7-129">It then calls the [**ImageList\_DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) function to unlock the window and hide the drag image, allowing the window to be updated.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e63d7-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e63d7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e63d7-131">Referência de listas de imagens</span><span class="sxs-lookup"><span data-stu-id="e63d7-131">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="e63d7-132">Sobre as listas de imagens</span><span class="sxs-lookup"><span data-stu-id="e63d7-132">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="e63d7-133">Usando listas de imagens</span><span class="sxs-lookup"><span data-stu-id="e63d7-133">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 