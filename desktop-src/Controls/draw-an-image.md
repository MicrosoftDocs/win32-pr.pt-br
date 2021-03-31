---
title: Como desenhar uma imagem
description: Este tópico demonstra como usar a função ImageList \_ draw para desenhar uma imagem.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917813"
---
# <a name="how-to-draw-an-image"></a><span data-ttu-id="451ee-103">Como desenhar uma imagem</span><span class="sxs-lookup"><span data-stu-id="451ee-103">How to Draw an Image</span></span>

<span data-ttu-id="451ee-104">Este tópico demonstra como usar a função [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para desenhar uma imagem.</span><span class="sxs-lookup"><span data-stu-id="451ee-104">This topic demonstrates how to use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="451ee-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="451ee-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="451ee-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="451ee-106">Technologies</span></span>

-   [<span data-ttu-id="451ee-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="451ee-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="451ee-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="451ee-108">Prerequisites</span></span>

-   <span data-ttu-id="451ee-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="451ee-109">C/C++</span></span>
-   <span data-ttu-id="451ee-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="451ee-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="451ee-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="451ee-111">Instructions</span></span>


<span data-ttu-id="451ee-112">Para desenhar uma imagem, use a função [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) .</span><span class="sxs-lookup"><span data-stu-id="451ee-112">To draw an image, you use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) or [**ImageList\_DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) function.</span></span> <span data-ttu-id="451ee-113">Você especifica o identificador para uma lista de imagens, o índice da imagem a ser desenhada, o identificador para o contexto do dispositivo de destino, um local dentro do contexto do dispositivo e um ou mais estilos de desenho.</span><span class="sxs-lookup"><span data-stu-id="451ee-113">You specify the handle to an image list, the index of the image to draw, the handle to the destination device context, a location within the device context, and one or more drawing styles.</span></span>

<span data-ttu-id="451ee-114">A função definida pelo usuário no exemplo de código C++ a seguir usa a função [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para desenhar uma imagem e salva as coordenadas do cliente do retângulo delimitador da imagem.</span><span class="sxs-lookup"><span data-stu-id="451ee-114">The user-defined function in the following C++ code example uses the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image and saves the client coordinates of the image's bounding rectangle.</span></span> <span data-ttu-id="451ee-115">Uma função subsequente usa o retângulo delimitador para determinar se o usuário clicou na imagem.</span><span class="sxs-lookup"><span data-stu-id="451ee-115">A subsequent function uses the bounding rectangle to determine whether the user has clicked on the image.</span></span>



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="451ee-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="451ee-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="451ee-117">Referência de listas de imagens</span><span class="sxs-lookup"><span data-stu-id="451ee-117">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="451ee-118">Sobre as listas de imagens</span><span class="sxs-lookup"><span data-stu-id="451ee-118">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="451ee-119">Usando listas de imagens</span><span class="sxs-lookup"><span data-stu-id="451ee-119">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 




