---
title: Portando greset
description: O OpenGL substitui a função GL de íris, greset, pelas funções, glPushAttrib e glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Portabilidade do íris GL, variáveis de estado
- portando do íris GL, variáveis de estado
- portando para OpenGL do íris GL, variáveis de estado
- Portabilidade do OpenGL do íris GL, variáveis de estado
- variáveis de estado
- Portabilidade do íris GL, função greset
- portando do íris GL, função greset
- portando para OpenGL do íris GL, função greset
- Portabilidade OpenGL do íris GL, função greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364181"
---
# <a name="porting-greset"></a><span data-ttu-id="06142-112">Portando greset</span><span class="sxs-lookup"><span data-stu-id="06142-112">Porting greset</span></span>

<span data-ttu-id="06142-113">O OpenGL substitui a função GL de íris, **greset**, pelas funções, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="06142-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="06142-114">Use essas funções para salvar e restaurar grupos de variáveis de estado.</span><span class="sxs-lookup"><span data-stu-id="06142-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="06142-115">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="06142-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="06142-116">Este exemplo usa uma constante de bits ou de uma operação simbólica, indicando quais grupos de variáveis de estado enviar por push para uma pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="06142-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="06142-117">Cada constante refere-se a um grupo de variáveis de estado.</span><span class="sxs-lookup"><span data-stu-id="06142-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="06142-118">A tabela a seguir mostra os grupos de atributos com seus nomes de constantes simbólicas equivalentes.</span><span class="sxs-lookup"><span data-stu-id="06142-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="06142-119">Para obter uma lista completa das variáveis de estado OpenGL associadas a cada constante, consulte [**glPushAttrib**](glpushattrib.md).</span><span class="sxs-lookup"><span data-stu-id="06142-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="06142-120">Atributo</span><span class="sxs-lookup"><span data-stu-id="06142-120">Attribute</span></span>                       | <span data-ttu-id="06142-121">Constante</span><span class="sxs-lookup"><span data-stu-id="06142-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="06142-122">valor de limpeza do buffer de acumulação</span><span class="sxs-lookup"><span data-stu-id="06142-122">accumulation buffer clear value</span></span> | <span data-ttu-id="06142-123">BIT de buffer do GL \_ Accum \_ \_</span><span class="sxs-lookup"><span data-stu-id="06142-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="06142-124">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="06142-124">color buffer</span></span>                    | <span data-ttu-id="06142-125">\_bit do \_ buffer de cores GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="06142-126">atual</span><span class="sxs-lookup"><span data-stu-id="06142-126">current</span></span>                         | <span data-ttu-id="06142-127">BIT do GL \_ atual \_</span><span class="sxs-lookup"><span data-stu-id="06142-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="06142-128">buffer de profundidade</span><span class="sxs-lookup"><span data-stu-id="06142-128">depth buffer</span></span>                    | <span data-ttu-id="06142-129">\_bit de \_ buffer de profundidade GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="06142-130">enable</span><span class="sxs-lookup"><span data-stu-id="06142-130">enable</span></span>                          | <span data-ttu-id="06142-131">\_bit de habilitação GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="06142-132">avaliadores</span><span class="sxs-lookup"><span data-stu-id="06142-132">evaluators</span></span>                      | <span data-ttu-id="06142-133">\_bit de Val EGL \_</span><span class="sxs-lookup"><span data-stu-id="06142-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="06142-134">neblina</span><span class="sxs-lookup"><span data-stu-id="06142-134">fog</span></span>                             | <span data-ttu-id="06142-135">\_bit de neblina GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="06142-136">Configuração da base da \_ lista GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="06142-137">\_bit da lista GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="06142-138">variáveis de dica</span><span class="sxs-lookup"><span data-stu-id="06142-138">hint variables</span></span>                  | <span data-ttu-id="06142-139">\_bit de dica GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="06142-140">variáveis de iluminação</span><span class="sxs-lookup"><span data-stu-id="06142-140">lighting variables</span></span>              | <span data-ttu-id="06142-141">\_bit de iluminação GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="06142-142">modo de desenho de linha</span><span class="sxs-lookup"><span data-stu-id="06142-142">line drawing mode</span></span>               | <span data-ttu-id="06142-143">\_bit de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="06142-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="06142-144">variáveis de modo de pixel</span><span class="sxs-lookup"><span data-stu-id="06142-144">pixel mode variables</span></span>            | <span data-ttu-id="06142-145">\_bit do \_ modo de pixel GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="06142-146">variáveis de ponto</span><span class="sxs-lookup"><span data-stu-id="06142-146">point variables</span></span>                 | <span data-ttu-id="06142-147">\_bit de ponto GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="06142-148">polygon</span><span class="sxs-lookup"><span data-stu-id="06142-148">polygon</span></span>                         | <span data-ttu-id="06142-149">\_bit do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="06142-150">Stipple de polígono</span><span class="sxs-lookup"><span data-stu-id="06142-150">polygon stipple</span></span>                 | <span data-ttu-id="06142-151">\_STIPPLE de polígono do GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="06142-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="06142-152">tesoura</span><span class="sxs-lookup"><span data-stu-id="06142-152">scissor</span></span>                         | <span data-ttu-id="06142-153">BIT GL de \_ tesoura \_</span><span class="sxs-lookup"><span data-stu-id="06142-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="06142-154">buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="06142-154">stencil buffer</span></span>                  | <span data-ttu-id="06142-155">\_bit de \_ buffer do estêncil GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="06142-156">textura</span><span class="sxs-lookup"><span data-stu-id="06142-156">texture</span></span>                         | <span data-ttu-id="06142-157">\_bit de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="06142-158">transformação</span><span class="sxs-lookup"><span data-stu-id="06142-158">transform</span></span>                       | <span data-ttu-id="06142-159">\_bit de transformação GL \_</span><span class="sxs-lookup"><span data-stu-id="06142-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="06142-160">visor</span><span class="sxs-lookup"><span data-stu-id="06142-160">viewport</span></span>                        | <span data-ttu-id="06142-161">\_bit GL viewport \_</span><span class="sxs-lookup"><span data-stu-id="06142-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="06142-162">GL \_ todos \_ os \_ bits de Atrib.</span><span class="sxs-lookup"><span data-stu-id="06142-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="06142-163">Para restaurar os valores das variáveis de estado para aquelas salvas com o último [**glPushAttrib**](glpushattrib.md), basta chamar [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="06142-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="06142-164">As variáveis que você não salvou permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="06142-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="06142-165">A pilha de atributos tem uma profundidade finita de pelo menos 16.</span><span class="sxs-lookup"><span data-stu-id="06142-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




