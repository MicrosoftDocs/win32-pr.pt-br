---
title: Transportando curvas de corte
description: As curvas de corte de OpenGL são muito semelhantes às curvas de corte do íris GL. A tabela a seguir lista as funções do íris GL para definir curvas de corte e suas funções OpenGL equivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Portagem do íris GL, curvas de corte
- portando do íris GL, aparando curvas
- portando para OpenGL do íris GL, aparando curvas
- Portabilidade do OpenGL do íris GL, corte de curvas
- aparando curvas
- curvas
- Portabilidade do íris GL, curvas
- portando do íris GL, curvas
- portando para OpenGL do íris GL, curvas
- Portabilidade OpenGL do íris GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160202"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="8688c-114">Transportando curvas de corte</span><span class="sxs-lookup"><span data-stu-id="8688c-114">Porting Trimming Curves</span></span>

<span data-ttu-id="8688c-115">As curvas de corte de OpenGL são muito semelhantes às curvas de corte do íris GL.</span><span class="sxs-lookup"><span data-stu-id="8688c-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="8688c-116">A tabela a seguir lista as funções do íris GL para definir curvas de corte e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8688c-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="8688c-117">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="8688c-117">IRIS GL function</span></span> | <span data-ttu-id="8688c-118">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="8688c-118">OpenGL function</span></span>                        | <span data-ttu-id="8688c-119">Significado</span><span class="sxs-lookup"><span data-stu-id="8688c-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="8688c-120">**bgntrim**</span><span class="sxs-lookup"><span data-stu-id="8688c-120">**bgntrim**</span></span>      | [<span data-ttu-id="8688c-121">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="8688c-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="8688c-122">Começa a definição da curva de corte.</span><span class="sxs-lookup"><span data-stu-id="8688c-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="8688c-123">**pwlcurve**</span><span class="sxs-lookup"><span data-stu-id="8688c-123">**pwlcurve**</span></span>     | [<span data-ttu-id="8688c-124">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="8688c-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="8688c-125">Define uma curva linear piecewise.</span><span class="sxs-lookup"><span data-stu-id="8688c-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="8688c-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="8688c-126">**nurbscurve**</span></span>   | [<span data-ttu-id="8688c-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="8688c-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="8688c-128">Especifica os atributos de curva de corte.</span><span class="sxs-lookup"><span data-stu-id="8688c-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="8688c-129">**endtrim**</span><span class="sxs-lookup"><span data-stu-id="8688c-129">**endtrim**</span></span>      | [<span data-ttu-id="8688c-130">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="8688c-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="8688c-131">Encerra a definição de curva de corte.</span><span class="sxs-lookup"><span data-stu-id="8688c-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="8688c-132">??</span><span class="sxs-lookup"><span data-stu-id="8688c-132">??</span></span>

 

 




