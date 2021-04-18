---
title: Portando o código de mesclagem
description: No íris GL, ao desenhar em buffers de frente e para trás, a mesclagem é feita com a leitura de um dos buffers, a mesclagem com essa cor e a gravação do resultado em ambos os buffers. No entanto, no OpenGL, cada buffer é lido por vez, mesclado e gravado.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Portabilidade do íris GL, mesclagem
- portando do íris GL, mesclagem
- portando para OpenGL do íris GL, mesclagem
- Portabilidade do OpenGL do íris GL, mesclagem
- combinação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753120"
---
# <a name="porting-blending-code"></a><span data-ttu-id="179e1-109">Portando o código de mesclagem</span><span class="sxs-lookup"><span data-stu-id="179e1-109">Porting Blending Code</span></span>

<span data-ttu-id="179e1-110">No íris GL, ao desenhar em buffers de frente e para trás, a mesclagem é feita com a leitura de um dos buffers, a mesclagem com essa cor e a gravação do resultado em ambos os buffers.</span><span class="sxs-lookup"><span data-stu-id="179e1-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="179e1-111">No entanto, no OpenGL, cada buffer é lido por vez, mesclado e gravado.</span><span class="sxs-lookup"><span data-stu-id="179e1-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="179e1-112">A tabela a seguir lista as funções de mesclagem íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="179e1-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="179e1-113">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="179e1-113">IRIS GL function</span></span>  | <span data-ttu-id="179e1-114">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="179e1-114">OpenGL function</span></span>                            | <span data-ttu-id="179e1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="179e1-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="179e1-116">[**glEnable**](glenable.md) (GL \_ Blend)</span><span class="sxs-lookup"><span data-stu-id="179e1-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="179e1-117">Ativa a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="179e1-117">Turns on blending.</span></span>          |
| <span data-ttu-id="179e1-118">**blendfunction**</span><span class="sxs-lookup"><span data-stu-id="179e1-118">**blendfunction**</span></span> | [<span data-ttu-id="179e1-119">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="179e1-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="179e1-120">Especifica uma função de mistura.</span><span class="sxs-lookup"><span data-stu-id="179e1-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="179e1-121">A função OpenGL **glBlendFunc** e a função **BLENDFUNCTION** do íris GL são quase idênticas.</span><span class="sxs-lookup"><span data-stu-id="179e1-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="179e1-122">A tabela a seguir lista os fatores de combinação do íris GL e seus equivalentes em OpenGL.</span><span class="sxs-lookup"><span data-stu-id="179e1-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="179e1-123">ÍRIS GL</span><span class="sxs-lookup"><span data-stu-id="179e1-123">IRIS GL</span></span>          | <span data-ttu-id="179e1-124">OpenGL</span><span class="sxs-lookup"><span data-stu-id="179e1-124">OpenGL</span></span>                     | <span data-ttu-id="179e1-125">Observações</span><span class="sxs-lookup"><span data-stu-id="179e1-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="179e1-126">BF \_ zero</span><span class="sxs-lookup"><span data-stu-id="179e1-126">BF\_ZERO</span></span>         | <span data-ttu-id="179e1-127">GL \_ zero</span><span class="sxs-lookup"><span data-stu-id="179e1-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="179e1-128">BF \_ um</span><span class="sxs-lookup"><span data-stu-id="179e1-128">BF\_ONE</span></span>          | <span data-ttu-id="179e1-129">GL \_ um</span><span class="sxs-lookup"><span data-stu-id="179e1-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="179e1-130">\_SA BF</span><span class="sxs-lookup"><span data-stu-id="179e1-130">BF\_SA</span></span>           | <span data-ttu-id="179e1-131">\_origem GL \_ alfa</span><span class="sxs-lookup"><span data-stu-id="179e1-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="179e1-132">MSA do BF \_</span><span class="sxs-lookup"><span data-stu-id="179e1-132">BF\_MSA</span></span>          | <span data-ttu-id="179e1-133">GL \_ um \_ menos \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="179e1-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="179e1-134">BF \_ da</span><span class="sxs-lookup"><span data-stu-id="179e1-134">BF\_DA</span></span>           | <span data-ttu-id="179e1-135">GL \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="179e1-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="179e1-136">MDA do BF \_</span><span class="sxs-lookup"><span data-stu-id="179e1-136">BF\_MDA</span></span>          | <span data-ttu-id="179e1-137">GL \_ um \_ menos o \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="179e1-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="179e1-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="179e1-138">BF\_SC</span></span>           | <span data-ttu-id="179e1-139">\_cor de src GL \_</span><span class="sxs-lookup"><span data-stu-id="179e1-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="179e1-140">BF \_ msc</span><span class="sxs-lookup"><span data-stu-id="179e1-140">BF\_MSC</span></span>          | <span data-ttu-id="179e1-141">GL \_ um \_ menos \_ cor de src \_</span><span class="sxs-lookup"><span data-stu-id="179e1-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="179e1-142">Somente destino.</span><span class="sxs-lookup"><span data-stu-id="179e1-142">Destination only.</span></span> |
| <span data-ttu-id="179e1-143">BF \_ DC</span><span class="sxs-lookup"><span data-stu-id="179e1-143">BF\_DC</span></span>           | <span data-ttu-id="179e1-144">\_cor de DST do GL \_</span><span class="sxs-lookup"><span data-stu-id="179e1-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="179e1-145">Somente origem.</span><span class="sxs-lookup"><span data-stu-id="179e1-145">Source only.</span></span>      |
| <span data-ttu-id="179e1-146">BF \_ MDC</span><span class="sxs-lookup"><span data-stu-id="179e1-146">BF\_MDC</span></span>          | <span data-ttu-id="179e1-147">GL \_ um \_ menos \_ cor do DST \_</span><span class="sxs-lookup"><span data-stu-id="179e1-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="179e1-148">Somente origem.</span><span class="sxs-lookup"><span data-stu-id="179e1-148">Source only.</span></span>      |
| <span data-ttu-id="179e1-149">\_ \_ MDA SA mínimo de BF \_</span><span class="sxs-lookup"><span data-stu-id="179e1-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="179e1-150">GL \_ src \_ alfa \_ saturado</span><span class="sxs-lookup"><span data-stu-id="179e1-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="179e1-151">??</span><span class="sxs-lookup"><span data-stu-id="179e1-151">??</span></span>

 

 




