---
description: Para desenhar um retângulo sombreado, defina uma matriz de trivértices com dois elementos e uma única estrutura de retângulo de GRADIENTe \_ . O exemplo de código a seguir mostra como desenhar um retângulo sombreado usando a função GradientFill com o modo de preenchimento de GRADIENTe \_ \_ definido.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Desenhando um retângulo sombreado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502425"
---
# <a name="drawing-a-shaded-rectangle"></a><span data-ttu-id="53b2a-104">Desenhando um retângulo sombreado</span><span class="sxs-lookup"><span data-stu-id="53b2a-104">Drawing a Shaded Rectangle</span></span>

<span data-ttu-id="53b2a-105">Para desenhar um retângulo sombreado, defina uma matriz de [**TRIvértices**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) com dois elementos e uma única estrutura de [**\_ retângulo de gradiente**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) .</span><span class="sxs-lookup"><span data-stu-id="53b2a-105">To draw a shaded rectangle, define a [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) array with two elements and a single [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) structure.</span></span> <span data-ttu-id="53b2a-106">O exemplo de código a seguir mostra como desenhar um retângulo sombreado usando a função [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) com o modo de preenchimento de gradiente \_ \_ definido.</span><span class="sxs-lookup"><span data-stu-id="53b2a-106">The following code example shows how to draw a shaded rectangle using the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function with the GRADIENT\_FILL\_RECT mode defined.</span></span>


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



<span data-ttu-id="53b2a-107">A imagem a seguir mostra a saída de desenho do exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="53b2a-107">The following image shows the drawing output of the preceding code example.</span></span>

![ilustração mostrando um retângulo com um preenchimento gradual de escuro no lado esquerdo para acender no lado direito](images/gradientfillrectangle.png)

## <a name="related-topics"></a><span data-ttu-id="53b2a-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53b2a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53b2a-110">Visão geral de bitmaps</span><span class="sxs-lookup"><span data-stu-id="53b2a-110">Bitmaps Overview</span></span>](bitmaps.md)
</dt> <dt>

[<span data-ttu-id="53b2a-111">Funções de bitmap</span><span class="sxs-lookup"><span data-stu-id="53b2a-111">Bitmap Functions</span></span>](bitmap-functions.md)
</dt> <dt>

[<span data-ttu-id="53b2a-112">Desenhando um triângulo sombreado</span><span class="sxs-lookup"><span data-stu-id="53b2a-112">Drawing a Shaded Triangle</span></span>](drawing-a-shaded-triangle.md)
</dt> <dt>

[<span data-ttu-id="53b2a-113">**EMRGRADIENTFILL**</span><span class="sxs-lookup"><span data-stu-id="53b2a-113">**EMRGRADIENTFILL**</span></span>](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[<span data-ttu-id="53b2a-114">**retângulo de GRADIENTe \_**</span><span class="sxs-lookup"><span data-stu-id="53b2a-114">**GRADIENT\_RECT**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[<span data-ttu-id="53b2a-115">**GradientFill**</span><span class="sxs-lookup"><span data-stu-id="53b2a-115">**GradientFill**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[<span data-ttu-id="53b2a-116">**Trivértice**</span><span class="sxs-lookup"><span data-stu-id="53b2a-116">**TRIVERTEX**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



