---
title: Portando viewports, Screenmasks e Scrboxes
description: As seguintes funções do visor do íris GL não têm nenhum equivalente em OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Portabilidade do íris GL, funções do visor
- portando do íris GL, funções do visor
- portando para OpenGL do íris GL, funções do visor
- Portabilidade do OpenGL do íris GL, funções do visor
- funções do visor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757497"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="183e4-108">Portando viewports, Screenmasks e Scrboxes</span><span class="sxs-lookup"><span data-stu-id="183e4-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="183e4-109">As seguintes funções do visor do íris GL não têm nenhum equivalente em OpenGL:</span><span class="sxs-lookup"><span data-stu-id="183e4-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="183e4-110">**reshapeviewport**</span><span class="sxs-lookup"><span data-stu-id="183e4-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="183e4-111">**scrbox**</span><span class="sxs-lookup"><span data-stu-id="183e4-111">**scrbox**</span></span>
-   <span data-ttu-id="183e4-112">**getscrbox**</span><span class="sxs-lookup"><span data-stu-id="183e4-112">**getscrbox**</span></span>

<span data-ttu-id="183e4-113">Com a função **viewport** GL do íris, você especifica as coordenadas x (em pixels) à esquerda e à direita de um retângulo do visor e as coordenadas y para as partes superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="183e4-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="183e4-114">No entanto, com a função OpenGL [**glViewport**](glviewport.md) , você especifica as coordenadas x e y (em pixels) do canto inferior esquerdo do retângulo do visor, juntamente com sua largura e altura.</span><span class="sxs-lookup"><span data-stu-id="183e4-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="183e4-115">A tabela a seguir lista as funções do viewport GL do íris e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="183e4-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="183e4-116">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="183e4-116">IRIS GL function</span></span>                          | <span data-ttu-id="183e4-117">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="183e4-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="183e4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="183e4-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="183e4-119">**visor** (esquerda, direita, inferior, superior)</span><span class="sxs-lookup"><span data-stu-id="183e4-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="183e4-120">[**glViewport**](glviewport.md) (x, y, largura, altura)</span><span class="sxs-lookup"><span data-stu-id="183e4-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="183e4-121">Define o visor.</span><span class="sxs-lookup"><span data-stu-id="183e4-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="183e4-122">**popviewportpushviewport**</span><span class="sxs-lookup"><span data-stu-id="183e4-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="183e4-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( \_ bit GL \_ viewport)</span><span class="sxs-lookup"><span data-stu-id="183e4-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="183e4-124">Envia e exibe a pilha.</span><span class="sxs-lookup"><span data-stu-id="183e4-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="183e4-125">**getviewport**</span><span class="sxs-lookup"><span data-stu-id="183e4-125">**getviewport**</span></span>                           | <span data-ttu-id="183e4-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ viewport)</span><span class="sxs-lookup"><span data-stu-id="183e4-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="183e4-127">Retorna dimensões do visor.</span><span class="sxs-lookup"><span data-stu-id="183e4-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="183e4-128">??</span><span class="sxs-lookup"><span data-stu-id="183e4-128">??</span></span>

 

 





