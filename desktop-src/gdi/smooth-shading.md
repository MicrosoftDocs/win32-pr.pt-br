---
description: O sombreamento suave é um método de sombreamento de uma região com um gradiente de cor.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Sombreamento suave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170534"
---
# <a name="smooth-shading"></a><span data-ttu-id="66ed6-103">Sombreamento suave</span><span class="sxs-lookup"><span data-stu-id="66ed6-103">Smooth Shading</span></span>

<span data-ttu-id="66ed6-104">O *sombreamento suave* é um método de sombreamento de uma região com um gradiente de cor.</span><span class="sxs-lookup"><span data-stu-id="66ed6-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="66ed6-105">Incluir informações de cor, junto com os limites de desenho primitivo, especifica o gradiente de cor.</span><span class="sxs-lookup"><span data-stu-id="66ed6-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="66ed6-106">A GDI interpola linearmente a cor do interior do primitivo passado nos pontos de extremidade de cor.</span><span class="sxs-lookup"><span data-stu-id="66ed6-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="66ed6-107">As informações de cor e vértice estão incluídas nas informações de posição na estrutura de [**TRIvértices**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .</span><span class="sxs-lookup"><span data-stu-id="66ed6-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="66ed6-108">Use a função [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) para preencher uma estrutura de triângulo ou de retângulo.</span><span class="sxs-lookup"><span data-stu-id="66ed6-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="66ed6-109">Para preencher um triângulo com sombreamento suave, chame **GradientFill** com os três pontos de extremidade do triângulo.</span><span class="sxs-lookup"><span data-stu-id="66ed6-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="66ed6-110">Para preencher um retângulo com sombreamento suave, chame **GradientFill** com as coordenadas de retângulo superior esquerda e inferior direita.</span><span class="sxs-lookup"><span data-stu-id="66ed6-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="66ed6-111">**GradientFill** faz referência às estruturas [**trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ retângulo de gradiente**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)e [**\_ triângulo de gradiente**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .</span><span class="sxs-lookup"><span data-stu-id="66ed6-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="66ed6-112">Para obter um exemplo, consulte [desenhando um triângulo sombreado](drawing-a-shaded-triangle.md).</span><span class="sxs-lookup"><span data-stu-id="66ed6-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



