---
title: Pontos de porta
description: O OpenGL não tem nenhum comando para desenhar um único ponto. Caso contrário, as funções de ponto de porta são simples. A tabela a seguir lista as funções do íris GL para pontos de desenho e suas funções OpenGL equivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Portabilidade do íris GL, pontos
- portando do íris GL, pontos
- portando para OpenGL do íris GL, pontos
- Portabilidade OpenGL do íris GL, pontos
- funções de desenho, pontos
- pontos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756709"
---
# <a name="porting-points"></a><span data-ttu-id="da2cc-111">Pontos de porta</span><span class="sxs-lookup"><span data-stu-id="da2cc-111">Porting Points</span></span>

<span data-ttu-id="da2cc-112">O OpenGL não tem nenhum comando para desenhar um único ponto.</span><span class="sxs-lookup"><span data-stu-id="da2cc-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="da2cc-113">Caso contrário, as funções de ponto de porta são simples.</span><span class="sxs-lookup"><span data-stu-id="da2cc-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="da2cc-114">A tabela a seguir lista as funções do íris GL para pontos de desenho e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="da2cc-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="da2cc-115">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="da2cc-115">IRIS GL function</span></span>           | <span data-ttu-id="da2cc-116">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="da2cc-116">OpenGL function</span></span>                                                   | <span data-ttu-id="da2cc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="da2cc-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2cc-118">**PNT**</span><span class="sxs-lookup"><span data-stu-id="da2cc-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="da2cc-119">Desenha um único ponto.</span><span class="sxs-lookup"><span data-stu-id="da2cc-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="da2cc-120">**bgnpoint**, **ponto de extremidade**</span><span class="sxs-lookup"><span data-stu-id="da2cc-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="da2cc-121">[**glBegin**](glbegin.md) ( \_ pontos GL), [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="da2cc-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="da2cc-122">Interpreta vértices como pontos.</span><span class="sxs-lookup"><span data-stu-id="da2cc-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="da2cc-123">**pntsize**</span><span class="sxs-lookup"><span data-stu-id="da2cc-123">**pntsize**</span></span>                | [<span data-ttu-id="da2cc-124">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="da2cc-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="da2cc-125">Define o tamanho do ponto em pixels.</span><span class="sxs-lookup"><span data-stu-id="da2cc-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="da2cc-126">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="da2cc-126">**pntsmooth**</span></span>              | <span data-ttu-id="da2cc-127">[**glEnable**](glenable.md) ( \_ sem ajuste de ponto GL \_ )</span><span class="sxs-lookup"><span data-stu-id="da2cc-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="da2cc-128">Ativa a suavização de ponto.</span><span class="sxs-lookup"><span data-stu-id="da2cc-128">Turns on point antialiasing.</span></span> <span data-ttu-id="da2cc-129">(Para obter mais informações sobre a suavização de ponto, consulte [portando funções de anti-aliasing](porting-antialiasing-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="da2cc-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="da2cc-130">Para obter informações sobre as funções Get relacionadas, consulte [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="da2cc-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="da2cc-131">??</span><span class="sxs-lookup"><span data-stu-id="da2cc-131">??</span></span>

 

 




