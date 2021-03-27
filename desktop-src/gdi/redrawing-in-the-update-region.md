---
description: Você pode limitar a quantidade de desenho que o aplicativo realiza ao processar a mensagem de pintura do WM \_ determinando o tamanho e o local da região de atualização.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Redesenhando na região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988783"
---
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="c52b1-103">Redesenhando na região de atualização</span><span class="sxs-lookup"><span data-stu-id="c52b1-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="c52b1-104">Você pode limitar a quantidade de desenho que o aplicativo realiza ao processar a mensagem de [**\_ pintura do WM**](wm-paint.md) determinando o tamanho e o local da região de atualização.</span><span class="sxs-lookup"><span data-stu-id="c52b1-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="c52b1-105">Como o sistema usa a região de atualização ao criar a região de recorte para o contexto do dispositivo de exibição da janela, você pode determinar indiretamente a região de atualização examinando a região de recorte.</span><span class="sxs-lookup"><span data-stu-id="c52b1-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="c52b1-106">No exemplo a seguir, o procedimento de janela desenha um triângulo, um retângulo, um Pentágono e um hexágono, mas somente se toda ou uma parte de cada figura estiver dentro da região de atualização.</span><span class="sxs-lookup"><span data-stu-id="c52b1-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="c52b1-107">O procedimento de janela usa a função [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) e um retângulo 100-por-100 para determinar se uma figura está dentro da região de recorte (e, portanto, a região de atualização) para o contexto de dispositivo comum recuperado por [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span><span class="sxs-lookup"><span data-stu-id="c52b1-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



<span data-ttu-id="c52b1-108">As coordenadas de cada figura neste exemplo se encontram dentro do mesmo retângulo 100-por-100.</span><span class="sxs-lookup"><span data-stu-id="c52b1-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="c52b1-109">Antes de desenhar uma figura, o procedimento de janela define a origem do visor para uma parte diferente da área do cliente usando a função [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) .</span><span class="sxs-lookup"><span data-stu-id="c52b1-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="c52b1-110">Isso impede que as figuras sejam desenhadas uma na parte superior da outra.</span><span class="sxs-lookup"><span data-stu-id="c52b1-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="c52b1-111">Alterar a origem do visor não afeta a região de recorte, mas afeta como as coordenadas do retângulo passado para [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) são interpretadas.</span><span class="sxs-lookup"><span data-stu-id="c52b1-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="c52b1-112">A alteração da origem também permite que você use um único retângulo para verificar a região de atualização em vez de retângulos individuais para cada figura.</span><span class="sxs-lookup"><span data-stu-id="c52b1-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



