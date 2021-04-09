---
description: Ao longo da programação Direct3D e Window, os objetos na tela são referidos em termos de retângulos delimitadores.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Retângulos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087244"
---
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="ec162-103">Retângulos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec162-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="ec162-104">Ao longo da programação Direct3D e Window, os objetos na tela são referidos em termos de retângulos delimitadores.</span><span class="sxs-lookup"><span data-stu-id="ec162-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="ec162-105">Os lados de um retângulo delimitador sempre são paralelos às laterais da tela, para que o retângulo possa ser descrito por dois pontos, o canto superior esquerdo e o canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="ec162-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="ec162-106">A maioria dos aplicativos usa a estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para transportar informações sobre um retângulo delimitador para uso durante a transferência para a tela ou para executar a detecção de clique.</span><span class="sxs-lookup"><span data-stu-id="ec162-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="ec162-107">Em C++, a estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) tem a definição a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec162-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="ec162-108">No exemplo anterior, os membros esquerdo e superior são as coordenadas x e y do canto superior esquerdo do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="ec162-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="ec162-109">Da mesma forma, os membros direito e inferior compõem as coordenadas do canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="ec162-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="ec162-110">A ilustração a seguir mostra como você pode visualizar esses valores.</span><span class="sxs-lookup"><span data-stu-id="ec162-110">The following illustration shows how you can visualize these values.</span></span>

![ilustração do retângulo delimitado pelos valores esquerdo, superior, direito e inferior](images/rect.png)

<span data-ttu-id="ec162-112">A coluna de pixels na borda direita e a linha de pixels na borda inferior não estão incluídas no RECT.</span><span class="sxs-lookup"><span data-stu-id="ec162-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="ec162-113">Por exemplo, bloquear um RECT com membros {10, 10, 138, 138} resulta em um objeto com 128 pixels em largura e altura.</span><span class="sxs-lookup"><span data-stu-id="ec162-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="ec162-114">No interesse da eficiência, da consistência e da facilidade de uso, todas as funções de apresentação do Direct3D funcionam com retângulos.</span><span class="sxs-lookup"><span data-stu-id="ec162-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec162-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec162-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec162-116">Coordenar sistemas e geometria</span><span class="sxs-lookup"><span data-stu-id="ec162-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
