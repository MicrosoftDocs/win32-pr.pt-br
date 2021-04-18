---
title: Grupos de atributos
description: Grupos de atributos
ms.assetid: 9fd7dc6e-6749-4e32-b795-21b63b64c291
keywords:
- OpenGL, grupos de atributos
- Referência OpenGL, grupos de atributos
- referência para OpenGL, grupos de atributos
- grupos de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d93582c8996438ad99d7bf896cf83bdf6fbf72d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783376"
---
# <a name="attribute-groups"></a><span data-ttu-id="95a2c-107">Grupos de atributos</span><span class="sxs-lookup"><span data-stu-id="95a2c-107">Attribute Groups</span></span>



| <span data-ttu-id="95a2c-108">Bit de máscara</span><span class="sxs-lookup"><span data-stu-id="95a2c-108">Mask bit</span></span>                  | <span data-ttu-id="95a2c-109">Grupo de atributos</span><span class="sxs-lookup"><span data-stu-id="95a2c-109">Attribute group</span></span> |
|---------------------------|-----------------|
| <span data-ttu-id="95a2c-110">BIT de buffer do GL \_ Accum \_ \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-110">GL\_ACCUM\_BUFFER\_BIT</span></span>    | <span data-ttu-id="95a2c-111">Accum-buffer</span><span class="sxs-lookup"><span data-stu-id="95a2c-111">accum-buffer</span></span>    |
| <span data-ttu-id="95a2c-112">GL \_ todos \_ os \_ bits de Atrib.</span><span class="sxs-lookup"><span data-stu-id="95a2c-112">GL\_ALL\_ATTRIB\_BITS</span></span>     |                 |
| <span data-ttu-id="95a2c-113">\_bit do \_ buffer de cores GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-113">GL\_COLOR\_BUFFER\_BIT</span></span>    | <span data-ttu-id="95a2c-114">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="95a2c-114">color-buffer</span></span>    |
| <span data-ttu-id="95a2c-115">BIT do GL \_ atual \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-115">GL\_CURRENT\_BIT</span></span>          | <span data-ttu-id="95a2c-116">atual</span><span class="sxs-lookup"><span data-stu-id="95a2c-116">current</span></span>         |
| <span data-ttu-id="95a2c-117">\_bit de \_ buffer de profundidade GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-117">GL\_DEPTH\_BUFFER\_BIT</span></span>    | <span data-ttu-id="95a2c-118">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="95a2c-118">depth-buffer</span></span>    |
| <span data-ttu-id="95a2c-119">\_bit de habilitação GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-119">GL\_ENABLE\_BIT</span></span>           | <span data-ttu-id="95a2c-120">enable</span><span class="sxs-lookup"><span data-stu-id="95a2c-120">enable</span></span>          |
| <span data-ttu-id="95a2c-121">\_bit de avaliação GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-121">GL\_EVAL\_BIT</span></span>             | <span data-ttu-id="95a2c-122">eval</span><span class="sxs-lookup"><span data-stu-id="95a2c-122">eval</span></span>            |
| <span data-ttu-id="95a2c-123">\_bit de neblina GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-123">GL\_FOG\_BIT</span></span>              | <span data-ttu-id="95a2c-124">neblina</span><span class="sxs-lookup"><span data-stu-id="95a2c-124">fog</span></span>             |
| <span data-ttu-id="95a2c-125">\_bit de dica GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-125">GL\_HINT\_BIT</span></span>             | <span data-ttu-id="95a2c-126">Dica de</span><span class="sxs-lookup"><span data-stu-id="95a2c-126">hint</span></span>            |
| <span data-ttu-id="95a2c-127">\_bit de iluminação GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-127">GL\_LIGHTING\_BIT</span></span>         | <span data-ttu-id="95a2c-128">iluminação</span><span class="sxs-lookup"><span data-stu-id="95a2c-128">lighting</span></span>        |
| <span data-ttu-id="95a2c-129">\_bit de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-129">GL\_LINE\_BIT</span></span>             | <span data-ttu-id="95a2c-130">line</span><span class="sxs-lookup"><span data-stu-id="95a2c-130">line</span></span>            |
| <span data-ttu-id="95a2c-131">\_bit da lista GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-131">GL\_LIST\_BIT</span></span>             | <span data-ttu-id="95a2c-132">list</span><span class="sxs-lookup"><span data-stu-id="95a2c-132">list</span></span>            |
| <span data-ttu-id="95a2c-133">\_bit do \_ modo de pixel GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-133">GL\_PIXEL\_MODE\_BIT</span></span>      | <span data-ttu-id="95a2c-134">pixel</span><span class="sxs-lookup"><span data-stu-id="95a2c-134">pixel</span></span>           |
| <span data-ttu-id="95a2c-135">\_bit de ponto GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-135">GL\_POINT\_BIT</span></span>            | <span data-ttu-id="95a2c-136">point</span><span class="sxs-lookup"><span data-stu-id="95a2c-136">point</span></span>           |
| <span data-ttu-id="95a2c-137">\_bit do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-137">GL\_POLYGON\_BIT</span></span>          | <span data-ttu-id="95a2c-138">polygon</span><span class="sxs-lookup"><span data-stu-id="95a2c-138">polygon</span></span>         |
| <span data-ttu-id="95a2c-139">\_STIPPLE de polígono do GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-139">GL\_POLYGON\_STIPPLE\_BIT</span></span> | <span data-ttu-id="95a2c-140">polígono-Stipple</span><span class="sxs-lookup"><span data-stu-id="95a2c-140">polygon-stipple</span></span> |
| <span data-ttu-id="95a2c-141">BIT GL de \_ tesoura \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-141">GL\_SCISSOR\_BIT</span></span>          | <span data-ttu-id="95a2c-142">tesoura</span><span class="sxs-lookup"><span data-stu-id="95a2c-142">scissor</span></span>         |
| <span data-ttu-id="95a2c-143">\_bit de \_ buffer do estêncil GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-143">GL\_STENCIL\_BUFFER\_BIT</span></span>  | <span data-ttu-id="95a2c-144">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="95a2c-144">stencil-buffer</span></span>  |
| <span data-ttu-id="95a2c-145">\_bit de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-145">GL\_TEXTURE\_BIT</span></span>          | <span data-ttu-id="95a2c-146">textura</span><span class="sxs-lookup"><span data-stu-id="95a2c-146">texture</span></span>         |
| <span data-ttu-id="95a2c-147">\_bit de transformação GL \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-147">GL\_TRANSFORM\_BIT</span></span>        | <span data-ttu-id="95a2c-148">transformação</span><span class="sxs-lookup"><span data-stu-id="95a2c-148">transform</span></span>       |
| <span data-ttu-id="95a2c-149">\_bit GL viewport \_</span><span class="sxs-lookup"><span data-stu-id="95a2c-149">GL\_VIEWPORT\_BIT</span></span>         | <span data-ttu-id="95a2c-150">visor</span><span class="sxs-lookup"><span data-stu-id="95a2c-150">viewport</span></span>        |



 

 

 




