---
title: Código de porta que precisa de uma posição de gráfico atual
description: O OpenGL não mantém uma posição gráfica atual. As funções da íris GL que dependem da posição de gráficos atual, como mover, desenhar e RMV, não têm equivalentes em OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Portabilidade do íris GL, posição de gráficos atual
- portando do íris GL, posição de gráficos atual
- portando para OpenGL do íris GL, posição de gráficos atual
- Portabilidade OpenGL do íris GL, posição de gráficos atual
- posição de gráficos atual
- posições de rasterização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "103638934"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="c3bdf-110">Código de porta que precisa de uma posição de gráfico atual</span><span class="sxs-lookup"><span data-stu-id="c3bdf-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="c3bdf-111">O OpenGL não mantém uma posição gráfica atual.</span><span class="sxs-lookup"><span data-stu-id="c3bdf-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="c3bdf-112">As funções da íris GL que dependem da posição de gráficos atual, como **mover**, **desenhar** e **RMV**, não têm equivalentes em OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c3bdf-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="c3bdf-113">Versões mais antigas do íris GL incluíam comandos de desenho que se basearam na posição de gráficos atual, embora seu uso tenha sido desencorajado.</span><span class="sxs-lookup"><span data-stu-id="c3bdf-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="c3bdf-114">Você precisará reescrever seu código se tiver confiado na posição gráfica atual de qualquer forma ou usar uma das seguintes rotinas:</span><span class="sxs-lookup"><span data-stu-id="c3bdf-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="c3bdf-115">**desenhar** e **mover**</span><span class="sxs-lookup"><span data-stu-id="c3bdf-115">**draw** and **move**</span></span>
-   <span data-ttu-id="c3bdf-116">**PMV**, **Laos** e **PCLOS**</span><span class="sxs-lookup"><span data-stu-id="c3bdf-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="c3bdf-117">**rdr**, **RMV**, **rpdr** e **rpmv**</span><span class="sxs-lookup"><span data-stu-id="c3bdf-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="c3bdf-118">**getgpos**</span><span class="sxs-lookup"><span data-stu-id="c3bdf-118">**getgpos**</span></span>

<span data-ttu-id="c3bdf-119">O OpenGL tem um conceito de posição de rasterização que corresponde à posição de caractere atual do íris GL.</span><span class="sxs-lookup"><span data-stu-id="c3bdf-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="c3bdf-120">Para obter mais informações sobre o posicionamento de rasterização, consulte [portando operações de pixel](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c3bdf-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="c3bdf-121">Este tópico inclui informações sobre o seguinte.</span><span class="sxs-lookup"><span data-stu-id="c3bdf-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="c3bdf-122">Comandos de limpeza de tela e buffer de portabilidade</span><span class="sxs-lookup"><span data-stu-id="c3bdf-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="c3bdf-123">Portando funções de matriz e transformação</span><span class="sxs-lookup"><span data-stu-id="c3bdf-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="c3bdf-124">Portando o código do modo MSINGLE</span><span class="sxs-lookup"><span data-stu-id="c3bdf-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="c3bdf-125">Funções de portabilidade que obtêm matrizes e transformações</span><span class="sxs-lookup"><span data-stu-id="c3bdf-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="c3bdf-126">Portando viewports, Screenmasks e Scrboxes</span><span class="sxs-lookup"><span data-stu-id="c3bdf-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="c3bdf-127">Portando planos de recorte</span><span class="sxs-lookup"><span data-stu-id="c3bdf-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




