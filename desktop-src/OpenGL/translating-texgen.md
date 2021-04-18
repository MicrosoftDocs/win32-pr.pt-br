---
title: Convertendo texgen
description: A função texgen do íris GL é convertida em glTexGen para OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
- Portabilidade do íris GL, texgen
- portando do íris GL, texgen
- portando para OpenGL do íris GL, texgen
- Portabilidade OpenGL do íris GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757097"
---
# <a name="translating-texgen"></a><span data-ttu-id="fb700-113">Convertendo texgen</span><span class="sxs-lookup"><span data-stu-id="fb700-113">Translating texgen</span></span>

<span data-ttu-id="fb700-114">A função **texgen** do íris GL é convertida em [glTexGen](gltexgen-functions.md) para OpenGL.</span><span class="sxs-lookup"><span data-stu-id="fb700-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="fb700-115">Com o íris GL, você chama **texgen** duas vezes: uma vez para definir o modo e a equação do plano simultaneamente, e uma vez para habilitar a geração da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="fb700-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="fb700-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fb700-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="fb700-117">Com o OpenGL, você faz três chamadas: dois para **glTexGen** (uma vez para definir o modo e uma vez para definir a equação de plano) e um para [**glEnable**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="fb700-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="fb700-118">Por exemplo, o OpenGL equivalente ao código de íris GL acima é:</span><span class="sxs-lookup"><span data-stu-id="fb700-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="fb700-119">A tabela a seguir lista os nomes de coordenadas de textura do íris GL e seus equivalentes em OpenGL.</span><span class="sxs-lookup"><span data-stu-id="fb700-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="fb700-120">Coordenada de textura do íris GL</span><span class="sxs-lookup"><span data-stu-id="fb700-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="fb700-121">Coordenada de textura OpenGL</span><span class="sxs-lookup"><span data-stu-id="fb700-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="fb700-122">argumento glEnable</span><span class="sxs-lookup"><span data-stu-id="fb700-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="fb700-123">\_S TX</span><span class="sxs-lookup"><span data-stu-id="fb700-123">TX\_S</span></span>                      | <span data-ttu-id="fb700-124">\_S GL</span><span class="sxs-lookup"><span data-stu-id="fb700-124">GL\_S</span></span>                     | <span data-ttu-id="fb700-125">S do GL \_ Texture \_ Gen \_</span><span class="sxs-lookup"><span data-stu-id="fb700-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="fb700-126">T de TX \_</span><span class="sxs-lookup"><span data-stu-id="fb700-126">TX\_T</span></span>                      | <span data-ttu-id="fb700-127">GL \_ T</span><span class="sxs-lookup"><span data-stu-id="fb700-127">GL\_T</span></span>                     | <span data-ttu-id="fb700-128">\_geração de textura de Texture GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb700-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="fb700-129">\_R TX</span><span class="sxs-lookup"><span data-stu-id="fb700-129">TX\_R</span></span>                      | <span data-ttu-id="fb700-130">GL \_ R</span><span class="sxs-lookup"><span data-stu-id="fb700-130">GL\_R</span></span>                     | <span data-ttu-id="fb700-131">o GL de \_ Texture \_ Gen \_ R</span><span class="sxs-lookup"><span data-stu-id="fb700-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="fb700-132">TX \_ Q</span><span class="sxs-lookup"><span data-stu-id="fb700-132">TX\_Q</span></span>                      | <span data-ttu-id="fb700-133">GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="fb700-133">GL\_Q</span></span>                     | <span data-ttu-id="fb700-134">GL \_ Texture \_ Gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="fb700-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="fb700-135">A tabela a seguir lista os modos de geração de textura do íris GL e seus modos de textura e nomes de plano do OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="fb700-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="fb700-136">Modo de textura do íris GL</span><span class="sxs-lookup"><span data-stu-id="fb700-136">IRIS GL texture mode</span></span> | <span data-ttu-id="fb700-137">Modo de textura OpenGL</span><span class="sxs-lookup"><span data-stu-id="fb700-137">OpenGL texture mode</span></span> | <span data-ttu-id="fb700-138">Nome do plano OpenGL</span><span class="sxs-lookup"><span data-stu-id="fb700-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="fb700-139">TG \_ linear</span><span class="sxs-lookup"><span data-stu-id="fb700-139">TG\_LINEAR</span></span>           | <span data-ttu-id="fb700-140">\_objeto GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="fb700-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="fb700-141">\_plano de objeto GL \_</span><span class="sxs-lookup"><span data-stu-id="fb700-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="fb700-142">delimitação de TG \_</span><span class="sxs-lookup"><span data-stu-id="fb700-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="fb700-143">olho do GL \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="fb700-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="fb700-144">\_plano de olho GL \_</span><span class="sxs-lookup"><span data-stu-id="fb700-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="fb700-145">TG \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="fb700-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="fb700-146">\_mapa de esfera GL \_</span><span class="sxs-lookup"><span data-stu-id="fb700-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




