---
title: Comandos de limpeza de tela e buffer de portabilidade
description: O OpenGL substitui uma variedade de funções do íris GL Clear (como zclear, aclear, sClear e assim por diante) por uma única função, glClear. Especifique exatamente o que você deseja limpar passando máscaras para glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Portabilidade do íris GL, limpar funções
- portando do íris GL, limpar funções
- portando para OpenGL do íris GL, limpar funções
- Portabilidade do OpenGL do íris GL, limpar funções
- limpar funções
- Portabilidade do íris GL, comandos de limpeza de tela
- portando do íris GL, comandos de limpeza de tela
- portando para OpenGL do íris GL, comandos de limpeza de tela
- Portabilidade OpenGL do íris GL, comandos de limpeza de tela
- comandos de limpeza de tela
- Portabilidade do íris GL, comandos de limpeza de buffer
- portando do íris GL, comandos de limpeza de buffer
- portando para OpenGL do íris GL, comandos de limpeza de buffer
- Portabilidade OpenGL do íris GL, comandos de limpeza de buffer
- comandos de limpeza de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753119"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="cb3de-119">Comandos de limpeza de tela e buffer de portabilidade</span><span class="sxs-lookup"><span data-stu-id="cb3de-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="cb3de-120">O OpenGL substitui uma variedade de funções do íris GL **Clear** (como **zclear**, **aclear**, **sClear** e assim por diante) por uma única função, [**glClear**](glclear.md).</span><span class="sxs-lookup"><span data-stu-id="cb3de-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="cb3de-121">Especifique exatamente o que você deseja limpar passando máscaras para **glClear**.</span><span class="sxs-lookup"><span data-stu-id="cb3de-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="cb3de-122">Tenha os seguintes pontos em mente ao portar comandos de tela e buffer:</span><span class="sxs-lookup"><span data-stu-id="cb3de-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="cb3de-123">O OpenGL mantém a limpeza das cores separadamente das cores de desenho, com chamadas como [**glClearColor**](glclearcolor.md) e [**glClearIndex**](glclearindex.md).</span><span class="sxs-lookup"><span data-stu-id="cb3de-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="cb3de-124">Certifique-se de definir a cor clara para cada buffer antes de apagar.</span><span class="sxs-lookup"><span data-stu-id="cb3de-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="cb3de-125">Em vez de usar uma das várias chamadas Clear nomeadas de forma diferente, agora você limpa vários buffers com uma chamada, [**glClear**](glclear.md), por **ou** encaixar máscaras de buffer.</span><span class="sxs-lookup"><span data-stu-id="cb3de-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="cb3de-126">Por exemplo, **czclear** é substituído por:</span><span class="sxs-lookup"><span data-stu-id="cb3de-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="cb3de-127">A íris GL faz referência ao polígono Stipple e à cor writemask.</span><span class="sxs-lookup"><span data-stu-id="cb3de-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="cb3de-128">O OpenGL ignora o polígono Stipple mas faz referência à cor writemask.</span><span class="sxs-lookup"><span data-stu-id="cb3de-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="cb3de-129">(A função **czclear** ignora o Stipple de polígono e a cor writemask.)</span><span class="sxs-lookup"><span data-stu-id="cb3de-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="cb3de-130">A tabela a seguir lista as várias funções do íris GL Clear com suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="cb3de-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="cb3de-131">Chamada do íris GL</span><span class="sxs-lookup"><span data-stu-id="cb3de-131">IRIS GL call</span></span>         | <span data-ttu-id="cb3de-132">Chamada OpenGL</span><span class="sxs-lookup"><span data-stu-id="cb3de-132">OpenGL call</span></span>                                                               | <span data-ttu-id="cb3de-133">Significado</span><span class="sxs-lookup"><span data-stu-id="cb3de-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="cb3de-134">**acbuf**(AC \_ limpa)</span><span class="sxs-lookup"><span data-stu-id="cb3de-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="cb3de-135">**glClear**(bit de buffer do GL \_ Accum \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="cb3de-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="cb3de-136">Limpe o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="cb3de-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="cb3de-137">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="cb3de-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="cb3de-138">Defina a cor nítida de RGBA.</span><span class="sxs-lookup"><span data-stu-id="cb3de-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="cb3de-139">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="cb3de-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="cb3de-140">Defina o índice de cor de limpeza.</span><span class="sxs-lookup"><span data-stu-id="cb3de-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="cb3de-141">**clear**</span><span class="sxs-lookup"><span data-stu-id="cb3de-141">**clear**</span></span>            | <span data-ttu-id="cb3de-142">**glClear**( \_ bit de buffer de cores GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="cb3de-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="cb3de-143">Limpe o buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="cb3de-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="cb3de-144">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="cb3de-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="cb3de-145">Especifique o valor de limpeza para o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="cb3de-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="cb3de-146">**zclear**</span><span class="sxs-lookup"><span data-stu-id="cb3de-146">**zclear**</span></span>           | <span data-ttu-id="cb3de-147">**glClear**(bit de buffer de profundidade do GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="cb3de-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="cb3de-148">Limpe o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="cb3de-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="cb3de-149">**czclear**</span><span class="sxs-lookup"><span data-stu-id="cb3de-149">**czclear**</span></span>          | <span data-ttu-id="cb3de-150">**glClear**(bit de buffer de cores GL GL \_ \_ nível de \_ \| \_ \_ memória \_</span><span class="sxs-lookup"><span data-stu-id="cb3de-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="cb3de-151">Limpe o buffer de cores e o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="cb3de-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="cb3de-152">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="cb3de-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="cb3de-153">Especifique os valores claros para o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="cb3de-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="cb3de-154">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="cb3de-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="cb3de-155">Especifique o valor de limpeza para o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="cb3de-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="cb3de-156">**sclear**</span><span class="sxs-lookup"><span data-stu-id="cb3de-156">**sclear**</span></span>           | <span data-ttu-id="cb3de-157">**glClear**( \_ bit de buffer do estêncil GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="cb3de-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="cb3de-158">Limpe o buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="cb3de-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="cb3de-159">Quando o código do íris GL usa **gclear** e **sClear**, você pode combiná-los em uma única chamada de **glClear** ; pode melhorar o desempenho do seu programa.</span><span class="sxs-lookup"><span data-stu-id="cb3de-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





