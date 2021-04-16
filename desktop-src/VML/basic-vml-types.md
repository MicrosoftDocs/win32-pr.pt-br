---
title: Tipos de VML básicos
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. Migre páginas da Web e aplicativos que dependem de VML para SVG ou outros padrões amplamente suportados.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Linguagem VML (VML), tipos básicos
- VML (linguagem VML), tipos básicos
- gráficos vetoriais, tipos básicos de VML
- Linguagem VML (VML), tipos
- VML (linguagem VML), tipos
- gráficos vetoriais, tipos de VML
- tipos de VML básicos
- tipo booliano
- tipo de fração
- tipo de ordenada
- tipo de comprimento
- tipo de medida
- tipo de ângulo
- tipo de cor
- tipo de fonte
- tipo de bitmap
- tipo de vetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104562340"
---
# <a name="basic-vml-types"></a><span data-ttu-id="f62e3-121">Tipos de VML básicos</span><span class="sxs-lookup"><span data-stu-id="f62e3-121">Basic VML Types</span></span>

<span data-ttu-id="f62e3-122">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f62e3-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f62e3-123">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f62e3-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f62e3-124">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f62e3-125">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f62e3-126">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f62e3-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f62e3-127">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f62e3-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f62e3-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="f62e3-128">**Contents**</span></span>

-   [<span data-ttu-id="f62e3-129">Introdução</span><span class="sxs-lookup"><span data-stu-id="f62e3-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f62e3-130">booleano</span><span class="sxs-lookup"><span data-stu-id="f62e3-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="f62e3-131">fração</span><span class="sxs-lookup"><span data-stu-id="f62e3-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="f62e3-132">ordenada</span><span class="sxs-lookup"><span data-stu-id="f62e3-132">ordinate</span></span>](#ordinate)
-   [<span data-ttu-id="f62e3-133">length</span><span class="sxs-lookup"><span data-stu-id="f62e3-133">length</span></span>](#length)
    -   [<span data-ttu-id="f62e3-134">Representações alternativas</span><span class="sxs-lookup"><span data-stu-id="f62e3-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="f62e3-135">mensura</span><span class="sxs-lookup"><span data-stu-id="f62e3-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="f62e3-136">Representações alternativas</span><span class="sxs-lookup"><span data-stu-id="f62e3-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="f62e3-137">angle</span><span class="sxs-lookup"><span data-stu-id="f62e3-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="f62e3-138">Representações alternativas</span><span class="sxs-lookup"><span data-stu-id="f62e3-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="f62e3-139">color</span><span class="sxs-lookup"><span data-stu-id="f62e3-139">color</span></span>](#color)
    -   [<span data-ttu-id="f62e3-140">Unidades de cores</span><span class="sxs-lookup"><span data-stu-id="f62e3-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="f62e3-141">Cores HTML</span><span class="sxs-lookup"><span data-stu-id="f62e3-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="f62e3-142">Cores do esquema</span><span class="sxs-lookup"><span data-stu-id="f62e3-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="f62e3-143">Cores do sistema</span><span class="sxs-lookup"><span data-stu-id="f62e3-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="f62e3-144">Cores puras</span><span class="sxs-lookup"><span data-stu-id="f62e3-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="f62e3-145">Ajustes de cores</span><span class="sxs-lookup"><span data-stu-id="f62e3-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="f62e3-146">la</span><span class="sxs-lookup"><span data-stu-id="f62e3-146">font</span></span>](#font)
-   [<span data-ttu-id="f62e3-147">bitmap</span><span class="sxs-lookup"><span data-stu-id="f62e3-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="f62e3-148">Formatos de arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="f62e3-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="f62e3-149">vetor</span><span class="sxs-lookup"><span data-stu-id="f62e3-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="f62e3-150">Introdução</span><span class="sxs-lookup"><span data-stu-id="f62e3-150">Introduction</span></span>

<span data-ttu-id="f62e3-151">Essa proposta usa um pequeno número de tipos básicos, listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f62e3-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="f62e3-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="f62e3-152">Type</span></span>                  | <span data-ttu-id="f62e3-153">Elemento</span><span class="sxs-lookup"><span data-stu-id="f62e3-153">Element</span></span>           | <span data-ttu-id="f62e3-154">Representação fundamental</span><span class="sxs-lookup"><span data-stu-id="f62e3-154">Fundamental Representation</span></span> | <span data-ttu-id="f62e3-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="f62e3-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f62e3-156">booleano</span><span class="sxs-lookup"><span data-stu-id="f62e3-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="f62e3-157">1 bit</span><span class="sxs-lookup"><span data-stu-id="f62e3-157">1 bit</span></span>                      | <span data-ttu-id="f62e3-158">Um valor booliano: true ou false.</span><span class="sxs-lookup"><span data-stu-id="f62e3-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="f62e3-159">fração</span><span class="sxs-lookup"><span data-stu-id="f62e3-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="f62e3-160">número 2 6</span><span class="sxs-lookup"><span data-stu-id="f62e3-160">number 2 6</span></span>                 | <span data-ttu-id="f62e3-161">Um valor numérico, dimensionado por 2 6 (65536) e armazenado como um inteiro assinado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="f62e3-162">ordenada</span><span class="sxs-lookup"><span data-stu-id="f62e3-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="f62e3-163">sinal de adição de inteiro de 30 bits</span><span class="sxs-lookup"><span data-stu-id="f62e3-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="f62e3-164">Parte de uma coordenada (por exemplo, em um caminho), os valores definidos por coord.</span><span class="sxs-lookup"><span data-stu-id="f62e3-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| [<span data-ttu-id="f62e3-165">length</span><span class="sxs-lookup"><span data-stu-id="f62e3-165">length</span></span>](#length)     |                   | [<span data-ttu-id="f62e3-166">MONETÁRIA</span><span class="sxs-lookup"><span data-stu-id="f62e3-166">EMU</span></span>](#length)             | <span data-ttu-id="f62e3-167">Um comprimento físico, como a largura de uma linha ou o tamanho de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="f62e3-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="f62e3-168">mensura</span><span class="sxs-lookup"><span data-stu-id="f62e3-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="f62e3-169">EMU ou número 2 6</span><span class="sxs-lookup"><span data-stu-id="f62e3-169">EMU or number 2 6</span></span>          | <span data-ttu-id="f62e3-170">Um comprimento físico, incluindo um número de pixels de dispositivo ou uma fração de alguma outra quantidade.</span><span class="sxs-lookup"><span data-stu-id="f62e3-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="f62e3-171">angle</span><span class="sxs-lookup"><span data-stu-id="f62e3-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="f62e3-172">graus de 2 6</span><span class="sxs-lookup"><span data-stu-id="f62e3-172">degrees 2 6</span></span>                | <span data-ttu-id="f62e3-173">Um ângulo; positivo é no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="f62e3-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="f62e3-174">color</span><span class="sxs-lookup"><span data-stu-id="f62e3-174">color</span></span>](#color)       | [<span data-ttu-id="f62e3-175">c</span><span class="sxs-lookup"><span data-stu-id="f62e3-175">c</span></span>](#color)       | <span data-ttu-id="f62e3-176">complex</span><span class="sxs-lookup"><span data-stu-id="f62e3-176">complex</span></span>                    | <span data-ttu-id="f62e3-177">Um elemento que permite que uma cor seja derivada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="f62e3-178">la</span><span class="sxs-lookup"><span data-stu-id="f62e3-178">font</span></span>](#font)         | [<span data-ttu-id="f62e3-179">la</span><span class="sxs-lookup"><span data-stu-id="f62e3-179">font</span></span>](#font)     | <span data-ttu-id="f62e3-180">complex</span><span class="sxs-lookup"><span data-stu-id="f62e3-180">complex</span></span>                    | <span data-ttu-id="f62e3-181">Uma descrição de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="f62e3-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="f62e3-182">bitmap</span><span class="sxs-lookup"><span data-stu-id="f62e3-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="f62e3-183">bitmap</span><span class="sxs-lookup"><span data-stu-id="f62e3-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="f62e3-184">href</span><span class="sxs-lookup"><span data-stu-id="f62e3-184">href</span></span>                       | <span data-ttu-id="f62e3-185">Uma referência a um arquivo de imagem externa.</span><span class="sxs-lookup"><span data-stu-id="f62e3-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="f62e3-186">vetor</span><span class="sxs-lookup"><span data-stu-id="f62e3-186">vector</span></span>](#vector)     | [<span data-ttu-id="f62e3-187">l</span><span class="sxs-lookup"><span data-stu-id="f62e3-187">v</span></span>](#vector)      | <span data-ttu-id="f62e3-188">complex</span><span class="sxs-lookup"><span data-stu-id="f62e3-188">complex</span></span>                    | <span data-ttu-id="f62e3-189">Uma descrição de um caminho de vetor</span><span class="sxs-lookup"><span data-stu-id="f62e3-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="f62e3-190">A "representação fundamental" é a representação de precisão mais alta que a proposta exige para manter uma implementação em conformidade; os dados serão perdidos se a implementação não puder representar os dados para a precisão necessária.</span><span class="sxs-lookup"><span data-stu-id="f62e3-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="f62e3-191">Os tipos de cor, fonte e vetor correspondem a elementos que, por sua conta, têm estrutura – de certa forma, não são tipos básicos; no entanto, é conveniente tratá-los como tal nessa proposta.</span><span class="sxs-lookup"><span data-stu-id="f62e3-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="f62e3-192">Cada tipo básico não complexo tem um elemento associado de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="f62e3-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="f62e3-193">Esses nomes de elementos são reservados e não podem ser usados para nenhuma outra finalidade dentro de extensões, mesmo que o uso esteja dentro de um elemento de extensão OnView = "Skip".</span><span class="sxs-lookup"><span data-stu-id="f62e3-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="f62e3-194">Por isso, é possível que uma implementação que encontra XML desconhecido forneça um armazenamento interno eficiente do XML desconhecido, desde que os valores estejam entre os elementos de "tipo".</span><span class="sxs-lookup"><span data-stu-id="f62e3-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="f62e3-195">No primeiro exemplo acima, a cadeia de caracteres "1,578" deve ser armazenada como uma sequência de caracteres (a implementação não sabe se é uma cadeia de caracteres ou um número); no segundo exemplo, o elemento fracionário indica que o conteúdo é um número, portanto, ele pode ser convertido na representação de fração de alta precisão.</span><span class="sxs-lookup"><span data-stu-id="f62e3-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="f62e3-196">Tipos complexos (incluindo bitmap) têm nomes de elementos associados que são usados para delimitar o valor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="f62e3-197">Isso simplifica a análise garantindo que as tarefas de análise mais complexas sejam associadas a marcas de elemento exclusivas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="f62e3-198">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="f62e3-199">booleano</span><span class="sxs-lookup"><span data-stu-id="f62e3-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="f62e3-200">Um valor booliano é representado como uma palavra-chave que indica o estado do sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f62e3-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="f62e3-201">As palavras-chave a seguir são definidas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-201">The following keywords are defined.</span></span>



| <span data-ttu-id="f62e3-202">Valor para verdadeiro</span><span class="sxs-lookup"><span data-stu-id="f62e3-202">Value for true</span></span> | <span data-ttu-id="f62e3-203">Valor para false</span><span class="sxs-lookup"><span data-stu-id="f62e3-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="f62e3-204">true</span><span class="sxs-lookup"><span data-stu-id="f62e3-204">true</span></span>           | <span data-ttu-id="f62e3-205">false</span><span class="sxs-lookup"><span data-stu-id="f62e3-205">false</span></span>           |
| <span data-ttu-id="f62e3-206">sim</span><span class="sxs-lookup"><span data-stu-id="f62e3-206">yes</span></span>            | <span data-ttu-id="f62e3-207">não</span><span class="sxs-lookup"><span data-stu-id="f62e3-207">no</span></span>              |
| <span data-ttu-id="f62e3-208">em</span><span class="sxs-lookup"><span data-stu-id="f62e3-208">on</span></span>             | <span data-ttu-id="f62e3-209">Desligar</span><span class="sxs-lookup"><span data-stu-id="f62e3-209">off</span></span>             |
| <span data-ttu-id="f62e3-210">t</span><span class="sxs-lookup"><span data-stu-id="f62e3-210">t</span></span>              | <span data-ttu-id="f62e3-211">f</span><span class="sxs-lookup"><span data-stu-id="f62e3-211">f</span></span>               |
| <span data-ttu-id="f62e3-212">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-212">1</span></span>              | <span data-ttu-id="f62e3-213">0</span><span class="sxs-lookup"><span data-stu-id="f62e3-213">0</span></span>               |



 

<span data-ttu-id="f62e3-214">Uma implementação pode gravar qualquer valor e deve reconhecer todos os valores.</span><span class="sxs-lookup"><span data-stu-id="f62e3-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="f62e3-215">Uma implementação é gratuita para alterar valores de uma representação para outra.</span><span class="sxs-lookup"><span data-stu-id="f62e3-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="f62e3-216">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="f62e3-217">fração</span><span class="sxs-lookup"><span data-stu-id="f62e3-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="f62e3-218">Todos os valores numéricos (ou seja, valores de quantidades com dimensão) dentro dessa proposta podem ser armazenados como inteiros, dimensionando-os por 2 6 (65536).</span><span class="sxs-lookup"><span data-stu-id="f62e3-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="f62e3-219">Um número pode ser fornecido neste formulário, com o sufixo f ou como um número decimal sem sufixo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="f62e3-220">Assim, os seguintes elementos hipotéticos representam o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="f62e3-221">Uma quantidade com o sufixo f deve ser um número inteiro; números fracionários não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="f62e3-222">O inteiro resultante deve ser representável como um número assinado do complemento de 32 bits 2; assim, o intervalo efetivo da representação é 32768 (na verdade, menor que 32768 e maior ou igual a-32768).</span><span class="sxs-lookup"><span data-stu-id="f62e3-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="f62e3-223">Uma implementação de conformidade é necessária para preservar valores que são expressos como valores f.</span><span class="sxs-lookup"><span data-stu-id="f62e3-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="f62e3-224">Os valores representados como números decimais podem ser convertidos em um valor f e armazenados dessa forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="f62e3-225">Um aplicativo tem permissão para registrar valores gerados internamente em qualquer unidade apropriada; no entanto, um valor lido em de um documento existente deve ser mantido para a precisão original completa ou deve ser convertido em um valor f.</span><span class="sxs-lookup"><span data-stu-id="f62e3-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="f62e3-226">Se a implementação não puder fazer isso, ela deverá avisar o usuário de que os dados podem ser perdidos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="f62e3-227">(É aceitável emitir um aviso desse tipo quando os dados gerados externamente são encontrados pela primeira vez.)</span><span class="sxs-lookup"><span data-stu-id="f62e3-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="f62e3-228">Quando um valor decimal é convertido em formato f, a implementação pode usar qualquer modo de arredondamento aritmético; no entanto, um número inteiro deve ser convertido para o formato f exatamente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="f62e3-229">É recomendável que as implementações convertam por arredondamento para menos infinito e que a conversão sempre seja exata.</span><span class="sxs-lookup"><span data-stu-id="f62e3-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="f62e3-230">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="f62e3-231">ordenada</span><span class="sxs-lookup"><span data-stu-id="f62e3-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="f62e3-232">As unidades do sistema de coordenadas estabelecido por coord são de algum tipo nominal, que é conhecido como ordenada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="f62e3-233">Essa é uma medida de comprimento, mas é usada somente em relação ao retângulo que o coord estabelece.</span><span class="sxs-lookup"><span data-stu-id="f62e3-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="f62e3-234">Qualquer valor do tipo ordenada será dimensionado pelos valores *w* e *h* de coord e a taxa resultante usada para estabelecer uma medida real no dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f62e3-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="f62e3-235">Uma implementação em conformidade deve ser capaz de lidar com valores de ordenada de até 30 bits de sinal de adição (ou seja, um inteiro com sinal de 31 bits, não um inteiro com sinal de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="f62e3-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="f62e3-236">No entanto, é recomendável que as implementações tentem produzir coordenadas para o caminho e elementos semelhantes que têm cerca de 16 bits de precisão.</span><span class="sxs-lookup"><span data-stu-id="f62e3-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="f62e3-237">Isso minimizará a chance de estouro negativo em uma implementação de não conformidade.</span><span class="sxs-lookup"><span data-stu-id="f62e3-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="f62e3-238">os valores de ordenada são sempre integrais.</span><span class="sxs-lookup"><span data-stu-id="f62e3-238">ordinate values are always integral.</span></span> <span data-ttu-id="f62e3-239">Um ponto decimal pode não aparecer em um valor do tipo ordenada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="f62e3-240">Nenhum especificador de unidade pode ser anexado aos valores do tipo ordenada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="f62e3-241">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="f62e3-242">comprimento</span><span class="sxs-lookup"><span data-stu-id="f62e3-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="f62e3-243">Um comprimento é uma medida do mundo real ou, às vezes, uma medida em pixels de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="f62e3-244">É recomendável que as implementações evitem o uso de pixels de dispositivo (px).</span><span class="sxs-lookup"><span data-stu-id="f62e3-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="f62e3-245">Todos os qualificadores de unidade [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) padrão são permitidos em um comprimento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="f62e3-246">Além disso, o qualificador da emu pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="f62e3-247">Esse qualificador refere-se a uma unidade – a EMU (unidade de métrica em inglês), que é um denominador comum das quantidades de medidas em uso generalizado em gráficos de computador.</span><span class="sxs-lookup"><span data-stu-id="f62e3-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="f62e3-248">A EMU é <sup>centímetro</sup> /914400, ou seja, há 914400 de Emu por polegada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="f62e3-249">A tabela a seguir lista o número de EMUs em um pequeno número de unidades geralmente encontradas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="f62e3-250">Número de EMUs</span><span class="sxs-lookup"><span data-stu-id="f62e3-250">Number of EMUs</span></span> | <span data-ttu-id="f62e3-251">Número por polegada</span><span class="sxs-lookup"><span data-stu-id="f62e3-251">Number per Inch</span></span> | <span data-ttu-id="f62e3-252">Número por milímetro</span><span class="sxs-lookup"><span data-stu-id="f62e3-252">Number per Millimeter</span></span> | <span data-ttu-id="f62e3-253">Descrição</span><span class="sxs-lookup"><span data-stu-id="f62e3-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="f62e3-254">360</span><span class="sxs-lookup"><span data-stu-id="f62e3-254">360</span></span>            |                 | <span data-ttu-id="f62e3-255">0,01</span><span class="sxs-lookup"><span data-stu-id="f62e3-255">0.01</span></span>                  | <span data-ttu-id="f62e3-256">HIMETRIC Win32</span><span class="sxs-lookup"><span data-stu-id="f62e3-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="f62e3-257">12700</span><span class="sxs-lookup"><span data-stu-id="f62e3-257">12700</span></span>          | <span data-ttu-id="f62e3-258">72</span><span class="sxs-lookup"><span data-stu-id="f62e3-258">72</span></span>              |                       | <span data-ttu-id="f62e3-259">empresas</span><span class="sxs-lookup"><span data-stu-id="f62e3-259">"point"</span></span>                 |
| <span data-ttu-id="f62e3-260">635</span><span class="sxs-lookup"><span data-stu-id="f62e3-260">635</span></span>            | <span data-ttu-id="f62e3-261">1440</span><span class="sxs-lookup"><span data-stu-id="f62e3-261">1440</span></span>            |                       | <span data-ttu-id="f62e3-262">TWIP Win32</span><span class="sxs-lookup"><span data-stu-id="f62e3-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="f62e3-263">762</span><span class="sxs-lookup"><span data-stu-id="f62e3-263">762</span></span>            | <span data-ttu-id="f62e3-264">1200</span><span class="sxs-lookup"><span data-stu-id="f62e3-264">1200</span></span>            |                       | <span data-ttu-id="f62e3-265">Impressora de alta resolução</span><span class="sxs-lookup"><span data-stu-id="f62e3-265">High-resolution printer</span></span> |



 

<span data-ttu-id="f62e3-266">Números fracionários de EMUs não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="f62e3-267">Qualquer medida deve ser representável como um número integral assinado de 32 bits de EMUs--isso limita a magnitude de uma medida a 2348 polegadas--cerca de 59 metros ou 65 metros.</span><span class="sxs-lookup"><span data-stu-id="f62e3-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="f62e3-268">Como as medidas sempre se referem ao tamanho de uma renderização em um dispositivo de saída de tamanho nominal da tela ou da página, elas sempre estarão dentro desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="f62e3-269">Observe, no entanto, que a representação não é apropriada para medidas do mundo real e que onde elas são registradas (por exemplo, para registrar o tamanho real de um caminho), alguma outra representação deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="f62e3-270">Uma implementação de conformidade é necessária para preservar valores que são exatamente números de EMUs.</span><span class="sxs-lookup"><span data-stu-id="f62e3-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="f62e3-271">Os valores representados de qualquer outra maneira podem ser convertidos em um valor de UME e armazenados dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="f62e3-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="f62e3-272">Um aplicativo tem permissão para registrar valores gerados internamente em qualquer unidade apropriada; no entanto, um valor lido em de um documento existente deve ser mantido para a precisão original completa ou deve ser convertido em um valor de UME.</span><span class="sxs-lookup"><span data-stu-id="f62e3-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="f62e3-273">Se a implementação não puder fazer isso, ela deverá avisar o usuário de que os dados podem ser perdidos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="f62e3-274">(É aceitável emitir um aviso desse tipo quando os dados gerados externamente são encontrados pela primeira vez.)</span><span class="sxs-lookup"><span data-stu-id="f62e3-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="f62e3-275">Na prática, os comprimentos físicos são usados para relativamente poucas medições nesta proposta.</span><span class="sxs-lookup"><span data-stu-id="f62e3-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="f62e3-276">Os dados que normalmente são mais importantes são os dados de caminho e são codificados no sistema de coordenadas definido, de acordo com a forma, por coord.</span><span class="sxs-lookup"><span data-stu-id="f62e3-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="f62e3-277">Representações alternativas</span><span class="sxs-lookup"><span data-stu-id="f62e3-277">Alternative representations</span></span>

<span data-ttu-id="f62e3-278">As representações de comprimento padrão de HTML são definidas por [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="f62e3-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="f62e3-279">As unidades relativas, com exceção do pixel, não são significativas no contexto no qual os comprimentos são usados nesta proposta e não devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="f62e3-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="f62e3-280">Se o documento registra o tamanho de pixel pretendido (destino), isso define a tradução de pixels para a EMU; caso contrário, o padrão de 90 dpi definido por [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="f62e3-281">Com exceção da UME, qualquer valor pode ser dado como uma fração decimal.</span><span class="sxs-lookup"><span data-stu-id="f62e3-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="f62e3-282">Quando um valor decimal é convertido em EMU, a implementação pode usar qualquer modo de arredondamento aritmético.</span><span class="sxs-lookup"><span data-stu-id="f62e3-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="f62e3-283">(A única maneira de um aplicativo de criação garantir um resultado específico é especificá-lo na Emu.)</span><span class="sxs-lookup"><span data-stu-id="f62e3-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="f62e3-284">Se nenhum especificador de unidade for fornecido em um valor de comprimento, a implementação deverá assumir a emu.</span><span class="sxs-lookup"><span data-stu-id="f62e3-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="f62e3-285">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="f62e3-286">medida</span><span class="sxs-lookup"><span data-stu-id="f62e3-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="f62e3-287">Uma medida é uma quantidade que pode ser um [comprimento](#length) ou uma [fração](#fraction).</span><span class="sxs-lookup"><span data-stu-id="f62e3-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="f62e3-288">Isso se assemelha bastante às medidas de comprimento HTML e CSS, que podem, em muitos casos, ser medidas físicas ou porcentagens de alguma outra quantidade.</span><span class="sxs-lookup"><span data-stu-id="f62e3-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="f62e3-289">Se nenhum especificador de unidade for fornecido, o valor deve ser considerado uma fração decimal (portanto, esse comportamento é herdado de fração, não de comprimento).</span><span class="sxs-lookup"><span data-stu-id="f62e3-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="f62e3-290">Diferentemente do comprimento, um valor de pixel tem um significado definido pelo contexto, portanto, a conversão para a emu normalmente é inadequada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="f62e3-291">Há três representações fundamentais possíveis que a implementação deve manter (ou seja, uma representação não pode ser convertida em outra sem perda de informações).</span><span class="sxs-lookup"><span data-stu-id="f62e3-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="f62e3-292">Um valor fracionário deve ser mantido no formato de [fração](#fraction) (um valor "f").</span><span class="sxs-lookup"><span data-stu-id="f62e3-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="f62e3-293">Um comprimento físico deve ser mantido na EMU.</span><span class="sxs-lookup"><span data-stu-id="f62e3-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="f62e3-294">Um valor de pixel deve ser mantido como um número inteiro de pixels.</span><span class="sxs-lookup"><span data-stu-id="f62e3-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="f62e3-295">Números fracionários de pixels não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="f62e3-296">Representações alternativas</span><span class="sxs-lookup"><span data-stu-id="f62e3-296">Alternative representations</span></span>

<span data-ttu-id="f62e3-297">Todas as representações alternativas de [fração](#fraction) e [comprimento](#length) são permitidas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="f62e3-298">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="f62e3-299">angle</span><span class="sxs-lookup"><span data-stu-id="f62e3-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="f62e3-300">A representação fundamental de um ângulo é um número de graus múltiplos por 2 6 (65536) e armazenada como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="f62e3-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="f62e3-301">Como o espaço de coordenadas é invertido (o eixo y positivo está inoperante), um ângulo no sentido horário é positivo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="f62e3-302">Uma implementação de conformidade é necessária para preservar a precisão total de tal valor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="f62e3-303">Uma implementação tem permissão para usar qualquer intervalo para ângulos e tem permissão para normalise um ângulo (por exemplo, de-180 a + 180 ou 0 a 360).</span><span class="sxs-lookup"><span data-stu-id="f62e3-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="f62e3-304">Não é necessário que as implementações sejam consistentes; no entanto, a representação integral de um ângulo não deve exceder o intervalo de um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f62e3-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="f62e3-305">O sufixo FD é usado para identificar essa representação de um ângulo (grau fracionário).</span><span class="sxs-lookup"><span data-stu-id="f62e3-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="f62e3-306">Observe que isso é diferenciado do sufixo f para uma fração sem dimensão, embora aritmética idêntica possa ser usada para dar suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="f62e3-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="f62e3-307">O padrão para um valor angular é um grau simples, ou seja, um valor não dimensionado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="f62e3-308">Isso também pode ser sinalizado com o sufixo "" (o símbolo de grau); no entanto, o uso disso depende de ter uma codificação de documento adequada – consequentemente, o sufixo graus também é definido como média graus.</span><span class="sxs-lookup"><span data-stu-id="f62e3-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="f62e3-309">O conjunto completo de possíveis suficientes é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f62e3-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="f62e3-310">Sufixo</span><span class="sxs-lookup"><span data-stu-id="f62e3-310">Suffix</span></span>       | <span data-ttu-id="f62e3-311">Fator de conversão</span><span class="sxs-lookup"><span data-stu-id="f62e3-311">Conversion Factor</span></span> | <span data-ttu-id="f62e3-312">Comentários</span><span class="sxs-lookup"><span data-stu-id="f62e3-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="f62e3-313">FD</span><span class="sxs-lookup"><span data-stu-id="f62e3-313">fd</span></span>           | <span data-ttu-id="f62e3-314">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-314">1</span></span>                 | <span data-ttu-id="f62e3-315">Representação interna de alta precisão</span><span class="sxs-lookup"><span data-stu-id="f62e3-315">High-precision internal representation</span></span> |
| <span data-ttu-id="f62e3-316">nenhum, graus,</span><span class="sxs-lookup"><span data-stu-id="f62e3-316">none, deg,</span></span>   | <span data-ttu-id="f62e3-317">65536</span><span class="sxs-lookup"><span data-stu-id="f62e3-317">65536</span></span>             | <span data-ttu-id="f62e3-318">Degrees</span><span class="sxs-lookup"><span data-stu-id="f62e3-318">Degrees</span></span>                                |
| <span data-ttu-id="f62e3-319">rad</span><span class="sxs-lookup"><span data-stu-id="f62e3-319">rad</span></span>          | <span data-ttu-id="f62e3-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="f62e3-320">65536pi/180</span></span>       | <span data-ttu-id="f62e3-321">Radians</span><span class="sxs-lookup"><span data-stu-id="f62e3-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="f62e3-322">Representações alternativas</span><span class="sxs-lookup"><span data-stu-id="f62e3-322">Alternative representations</span></span>

<span data-ttu-id="f62e3-323">A transformação de dimensionamento tem descontinuidades em múltiplos estranhos de 45.</span><span class="sxs-lookup"><span data-stu-id="f62e3-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="f62e3-324">Portanto, é extremamente importante que a conversão de qualquer quantidade inexata seja bem definida.</span><span class="sxs-lookup"><span data-stu-id="f62e3-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="f62e3-325">Por esse motivo, a aritmética de conversão é definida para arredondar em direção a menos infinito.</span><span class="sxs-lookup"><span data-stu-id="f62e3-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="f62e3-326">Como isso pode ser difícil ou impossível de garantir em algumas implementações, o uso do seguinte é definido para ser um recurso de nível 3:</span><span class="sxs-lookup"><span data-stu-id="f62e3-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="f62e3-327">Qualquer valor de grau fracionário.</span><span class="sxs-lookup"><span data-stu-id="f62e3-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="f62e3-328">Qualquer valor de radianos</span><span class="sxs-lookup"><span data-stu-id="f62e3-328">Any radian value</span></span>

<span data-ttu-id="f62e3-329">Assim, os valores são qualificados FD e valores integrais não qualificados, ou valores integral qualificados graus ou devem ser tratados exatamente por uma implementação de nível 0 de conformidade; outros valores não precisam.</span><span class="sxs-lookup"><span data-stu-id="f62e3-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="f62e3-330">É altamente recomendável que qualquer implementação manipule a conversão de um valor de grau fracionário para um valor de grau em escala (FD) exatamente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="f62e3-331">Isso pode ser feito sem o suporte de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f62e3-331">This can be done without floating point support.</span></span>

<span data-ttu-id="f62e3-332">Os requisitos mais exagindo para conversão distingue FD da f.</span><span class="sxs-lookup"><span data-stu-id="f62e3-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="f62e3-333">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="f62e3-334">cor</span><span class="sxs-lookup"><span data-stu-id="f62e3-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="f62e3-335">As cores são uma parte essencial dos gráficos de computadores modernos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="f62e3-336">A proposta usa os métodos estabelecidos para especificar cores fixas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="f62e3-337">No entanto, as cores em diagramas raramente são cores estáticas simples; Geralmente, eles são derivados de outros elementos no diagrama.</span><span class="sxs-lookup"><span data-stu-id="f62e3-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="f62e3-338">Grande parte dessas informações é muito específica do aplicativo, portanto, essa proposta fornece dois mecanismos muito básicos para especificar esse comportamento:</span><span class="sxs-lookup"><span data-stu-id="f62e3-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="f62e3-339">Uma cor pode ser derivada de outra cor na mesma forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="f62e3-340">Um pequeno número de operações aritméticas é definido para derivar ou modificar uma cor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="f62e3-341">O mecanismo de forma de protótipo complementa isso permitindo que os protótipos sejam definidos a partir dos quais as cores podem ser herdadas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="f62e3-342">Um valor de cor é um superconjunto da [definição de cor CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="f62e3-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="f62e3-343">As extensões permitem que o valor de cor RGB seja determinado de outras cores dentro da forma ou de um esquema de cores geral definido usando CSS1.</span><span class="sxs-lookup"><span data-stu-id="f62e3-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="f62e3-344">Se o valor de um elemento for definido para ser uma cor, o *conteúdo* de um elemento definirá o valor de cor por meio de um único token de cor, opcionalmente modificado por uma operação aritmética na cor RGB correspondente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="f62e3-345">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="f62e3-346">Unidades de cores</span><span class="sxs-lookup"><span data-stu-id="f62e3-346">Color units</span></span>

<span data-ttu-id="f62e3-347">O conjunto completo de tokens de cor é proveniente de uma variedade de fontes: HTML, CSS1 e esta proposta.</span><span class="sxs-lookup"><span data-stu-id="f62e3-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="f62e3-348">Eles são definidos da seguinte maneira usando a notação de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) ou a notação XPointer definida para vinculação XML.</span><span class="sxs-lookup"><span data-stu-id="f62e3-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="f62e3-349">Nas definições de XPointer, a origem local é o elemento que contém o valor de cor e a expressão se refere a todo o conjunto de elementos da forma como se qualquer elemento de protótipo base tivesse sido mesclado com a forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="f62e3-350">Quando o elemento correspondente não existir, o valor padrão desse elemento será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="f62e3-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="f62e3-351">Cor</span><span class="sxs-lookup"><span data-stu-id="f62e3-351">Color</span></span>            | <span data-ttu-id="f62e3-352">Definição</span><span class="sxs-lookup"><span data-stu-id="f62e3-352">Definition</span></span>                                                                                                  | <span data-ttu-id="f62e3-353">Nível</span><span class="sxs-lookup"><span data-stu-id="f62e3-353">Level</span></span> | <span data-ttu-id="f62e3-354">Descrição</span><span class="sxs-lookup"><span data-stu-id="f62e3-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62e3-355">name</span><span class="sxs-lookup"><span data-stu-id="f62e3-355">name</span></span>             | <span data-ttu-id="f62e3-356">Veja abaixo</span><span class="sxs-lookup"><span data-stu-id="f62e3-356">See below</span></span>                                                                                                   | <span data-ttu-id="f62e3-357">0</span><span class="sxs-lookup"><span data-stu-id="f62e3-357">0</span></span>     | <span data-ttu-id="f62e3-358">Nome da cor HTML, conforme listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f62e3-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="f62e3-359">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="f62e3-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="f62e3-360">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="f62e3-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="f62e3-361">0</span><span class="sxs-lookup"><span data-stu-id="f62e3-361">0</span></span>     | <span data-ttu-id="f62e3-362">Representação de cor padrão CSS1/sRGB usando valores no intervalo 0.. 255 representados usando 2 dígitos hexadecimais cada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="f62e3-363">\#RGB</span><span class="sxs-lookup"><span data-stu-id="f62e3-363">\#rgb</span></span>            | <span data-ttu-id="f62e3-364">\#RRGGBB</span><span class="sxs-lookup"><span data-stu-id="f62e3-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="f62e3-365">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-365">1</span></span>     | <span data-ttu-id="f62e3-366">O formulário CSS1 foi reduzido com apenas três dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="f62e3-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="f62e3-367">RGB (r, g, b)</span><span class="sxs-lookup"><span data-stu-id="f62e3-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="f62e3-368">\#d m b</span><span class="sxs-lookup"><span data-stu-id="f62e3-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="f62e3-369">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-369">1</span></span>     | <span data-ttu-id="f62e3-370">Formulário CSS1 RGB; os elementos do valor RGB são convertidos conforme definido em [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="f62e3-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="f62e3-371">fill</span><span class="sxs-lookup"><span data-stu-id="f62e3-371">fill</span></span>             | <span data-ttu-id="f62e3-372">ancestral (1, forma)</span><span class="sxs-lookup"><span data-stu-id="f62e3-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="f62e3-373">filho (1, preenchimento)</span><span class="sxs-lookup"><span data-stu-id="f62e3-373">child(1, fill)</span></span><br/> <span data-ttu-id="f62e3-374">filho (1, cor)</span><span class="sxs-lookup"><span data-stu-id="f62e3-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="f62e3-375">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-375">1</span></span>     | <span data-ttu-id="f62e3-376">A cor de preenchimento do primeiro plano da forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="f62e3-377">fillBack</span><span class="sxs-lookup"><span data-stu-id="f62e3-377">fillBack</span></span>         | <span data-ttu-id="f62e3-378">ancestral (1, forma)</span><span class="sxs-lookup"><span data-stu-id="f62e3-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="f62e3-379">filho (1, preenchimento)</span><span class="sxs-lookup"><span data-stu-id="f62e3-379">child(1, fill)</span></span><br/> <span data-ttu-id="f62e3-380">filho (1, voltar)</span><span class="sxs-lookup"><span data-stu-id="f62e3-380">child(1, back)</span></span><br/> <span data-ttu-id="f62e3-381">filho (1, cor)</span><span class="sxs-lookup"><span data-stu-id="f62e3-381">child(1, color)</span></span><br/> | <span data-ttu-id="f62e3-382">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-382">1</span></span>     | <span data-ttu-id="f62e3-383">A cor do plano de fundo do preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="f62e3-384">line</span><span class="sxs-lookup"><span data-stu-id="f62e3-384">line</span></span>             | <span data-ttu-id="f62e3-385">ancestral (1, forma)</span><span class="sxs-lookup"><span data-stu-id="f62e3-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="f62e3-386">filho (1, linha)</span><span class="sxs-lookup"><span data-stu-id="f62e3-386">child(1, line)</span></span><br/> <span data-ttu-id="f62e3-387">filho (1, cor)</span><span class="sxs-lookup"><span data-stu-id="f62e3-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="f62e3-388">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-388">1</span></span>     | <span data-ttu-id="f62e3-389">A cor da linha de primeiro plano da forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="f62e3-390">lineBack</span><span class="sxs-lookup"><span data-stu-id="f62e3-390">lineBack</span></span>         | <span data-ttu-id="f62e3-391">ancestral (1, forma)</span><span class="sxs-lookup"><span data-stu-id="f62e3-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="f62e3-392">filho (1, linha)</span><span class="sxs-lookup"><span data-stu-id="f62e3-392">child(1, line)</span></span><br/> <span data-ttu-id="f62e3-393">filho (1, voltar)</span><span class="sxs-lookup"><span data-stu-id="f62e3-393">child(1,back)</span></span> <br/> <span data-ttu-id="f62e3-394">filho (1, cor)</span><span class="sxs-lookup"><span data-stu-id="f62e3-394">child(1, color)</span></span><br/> | <span data-ttu-id="f62e3-395">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-395">1</span></span>     | <span data-ttu-id="f62e3-396">A cor da linha do plano de fundo da forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="f62e3-397">lineOrFill</span><span class="sxs-lookup"><span data-stu-id="f62e3-397">lineOrFill</span></span>       | <span data-ttu-id="f62e3-398">linha, preenchimento</span><span class="sxs-lookup"><span data-stu-id="f62e3-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="f62e3-399">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-399">1</span></span>     | <span data-ttu-id="f62e3-400">O valor da linha, se não for padronizado, caso contrário, o valor de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="f62e3-401">Isso efetivamente retorna a cor que está na borda da forma.</span><span class="sxs-lookup"><span data-stu-id="f62e3-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="f62e3-402">fillThenLine</span><span class="sxs-lookup"><span data-stu-id="f62e3-402">fillThenLine</span></span>     | <span data-ttu-id="f62e3-403">preenchimento, linha</span><span class="sxs-lookup"><span data-stu-id="f62e3-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="f62e3-404">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-404">1</span></span>     | <span data-ttu-id="f62e3-405">O valor de preenchimento, se não for padronizado, caso contrário, o valor da linha.</span><span class="sxs-lookup"><span data-stu-id="f62e3-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="f62e3-406">Isso efetivamente retorna a cor da forma principal (se a forma não estiver preenchida, o resultado será a cor da linha).</span><span class="sxs-lookup"><span data-stu-id="f62e3-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="f62e3-407">shadow</span><span class="sxs-lookup"><span data-stu-id="f62e3-407">shadow</span></span>           | <span data-ttu-id="f62e3-408">ancestral (1, forma)</span><span class="sxs-lookup"><span data-stu-id="f62e3-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="f62e3-409">filho (1, sombra)</span><span class="sxs-lookup"><span data-stu-id="f62e3-409">child(1, shadow)</span></span><br/> <span data-ttu-id="f62e3-410">filho (1, cor)</span><span class="sxs-lookup"><span data-stu-id="f62e3-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="f62e3-411">2</span><span class="sxs-lookup"><span data-stu-id="f62e3-411">2</span></span>     | <span data-ttu-id="f62e3-412">A cor da sombra (esse é um recurso de nível 2).</span><span class="sxs-lookup"><span data-stu-id="f62e3-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="f62e3-413">scheme</span><span class="sxs-lookup"><span data-stu-id="f62e3-413">scheme</span></span>           | <span data-ttu-id="f62e3-414">Veja abaixo</span><span class="sxs-lookup"><span data-stu-id="f62e3-414">See below</span></span>                                                                                                   | <span data-ttu-id="f62e3-415">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-415">1</span></span>     | <span data-ttu-id="f62e3-416">Uma cor do esquema do esquema definido para o documento; Veja abaixo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="f62e3-417">esquema (*índice*)</span><span class="sxs-lookup"><span data-stu-id="f62e3-417">scheme(*index*)</span></span>  | <span data-ttu-id="f62e3-418">Veja abaixo</span><span class="sxs-lookup"><span data-stu-id="f62e3-418">See below</span></span>                                                                                                   | <span data-ttu-id="f62e3-419">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-419">1</span></span>     | <span data-ttu-id="f62e3-420">*Índice* de cores do esquema, começando em 0; Veja abaixo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="f62e3-421">this</span><span class="sxs-lookup"><span data-stu-id="f62e3-421">this</span></span>             | <span data-ttu-id="f62e3-422">Implícita</span><span class="sxs-lookup"><span data-stu-id="f62e3-422">Implied</span></span>                                                                                                     | <span data-ttu-id="f62e3-423">2</span><span class="sxs-lookup"><span data-stu-id="f62e3-423">2</span></span>     | <span data-ttu-id="f62e3-424">A operação (preencher um caminho ou desenhá-la) é definida de alguma outra maneira (por exemplo, como um bitmap) e a cor especifica uma "modificação" nas cores, portanto implícita.</span><span class="sxs-lookup"><span data-stu-id="f62e3-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="f62e3-425">paleta (*índice*)</span><span class="sxs-lookup"><span data-stu-id="f62e3-425">palette(*index*)</span></span> | <span data-ttu-id="f62e3-426">Implícita</span><span class="sxs-lookup"><span data-stu-id="f62e3-426">Implied</span></span>                                                                                                     | <span data-ttu-id="f62e3-427">3</span><span class="sxs-lookup"><span data-stu-id="f62e3-427">3</span></span>     | <span data-ttu-id="f62e3-428">Se comporta da mesma maneira, exceto que exatamente uma entrada em uma tabela de cores de bitmap é identificada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="f62e3-429">Permitido apenas onde explicitamente declarado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="f62e3-430">nenhum</span><span class="sxs-lookup"><span data-stu-id="f62e3-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="f62e3-431">2</span><span class="sxs-lookup"><span data-stu-id="f62e3-431">2</span></span>     | <span data-ttu-id="f62e3-432">Indica a ausência de uma cor; pode ser usado para cancelar uma operação de desenho que usa a cor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="f62e3-433">sistema</span><span class="sxs-lookup"><span data-stu-id="f62e3-433">system</span></span>           | <span data-ttu-id="f62e3-434">Veja abaixo</span><span class="sxs-lookup"><span data-stu-id="f62e3-434">See below</span></span>                                                                                                   | <span data-ttu-id="f62e3-435">3</span><span class="sxs-lookup"><span data-stu-id="f62e3-435">3</span></span>     | <span data-ttu-id="f62e3-436">Uma cor definida pela interface do usuário do sistema.</span><span class="sxs-lookup"><span data-stu-id="f62e3-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="f62e3-437">Essa cor permite que um valor de cor especifique uma modificação em uma cor que seja derivada de alguma outra maneira; em particular, uma única operação pode ser especificada para todas as cores em um bitmap.</span><span class="sxs-lookup"><span data-stu-id="f62e3-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="f62e3-438">A cor da paleta (*índice*) identifica uma determinada entrada em um bitmap mapeado para a paleta.</span><span class="sxs-lookup"><span data-stu-id="f62e3-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="f62e3-439">O uso dele só é definido para gravar uma entrada de tabela de cores que deve ser considerada transparente nesse bitmap.</span><span class="sxs-lookup"><span data-stu-id="f62e3-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="f62e3-440">A definição de um valor de cor não deve se referir, direta ou indiretamente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="f62e3-441">Se essa definição for encontrada, é recomendável, mas não necessária, que a implementação trate o valor indefinido como preto.</span><span class="sxs-lookup"><span data-stu-id="f62e3-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="f62e3-442">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="f62e3-443">Cores HTML</span><span class="sxs-lookup"><span data-stu-id="f62e3-443">HTML colors</span></span>

<span data-ttu-id="f62e3-444">O [HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) define os dezesseis nomes de cor a seguir:</span><span class="sxs-lookup"><span data-stu-id="f62e3-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="f62e3-445">Nomes de cor e valores sRGB</span><span class="sxs-lookup"><span data-stu-id="f62e3-445">Color names and sRGB values</span></span>

![Exemplo de cor preta.](images/black.gif)

<span data-ttu-id="f62e3-447">Black = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="f62e3-447">Black = "\#000000"</span></span>

![Exemplo de cor verde.](images/green.gif)

<span data-ttu-id="f62e3-449">Verde = " \# 008000"</span><span class="sxs-lookup"><span data-stu-id="f62e3-449">Green = "\#008000"</span></span>

![Exemplo de cor prateada.](images/silver.gif)

<span data-ttu-id="f62e3-451">Prata = " \# C0C0C0"</span><span class="sxs-lookup"><span data-stu-id="f62e3-451">Silver = "\#C0C0C0"</span></span>

![Exemplo de cor de verde-limão.](images/lime.gif)

<span data-ttu-id="f62e3-453">Verde-limão = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="f62e3-453">Lime = "\#00FF00"</span></span>

![Exemplo de cor cinza.](images/gray.gif)

<span data-ttu-id="f62e3-455">Cinza = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="f62e3-455">Gray = "\#808080"</span></span>

![Exemplo de cor de verde-oliva.](images/olive.gif)

<span data-ttu-id="f62e3-457">Verde-oliva = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="f62e3-457">Olive = "\#808000"</span></span>

![Exemplo de cor branca.](images/white.gif)

<span data-ttu-id="f62e3-459">Branco = " \# FFFFFF"</span><span class="sxs-lookup"><span data-stu-id="f62e3-459">White = "\#FFFFFF"</span></span>

![Exemplo de cor de ywllow.](images/yellow.gif)

<span data-ttu-id="f62e3-461">Amarelo = " \# FFFF00"</span><span class="sxs-lookup"><span data-stu-id="f62e3-461">Yellow = "\#FFFF00"</span></span>

![Exemplo de cor de bordô.](images/maroon.gif)

<span data-ttu-id="f62e3-463">Bordô = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="f62e3-463">Maroon = "\#800000"</span></span>

![Exemplo de cor azul.](images/navy.gif)

<span data-ttu-id="f62e3-465">Azul = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="f62e3-465">Navy = "\#000080"</span></span>

![Exemplo de cor vermelha.](images/red.gif)

<span data-ttu-id="f62e3-467">Vermelho = " \# FF0000"</span><span class="sxs-lookup"><span data-stu-id="f62e3-467">Red = "\#FF0000"</span></span>

![Exemplo de cor azul.](images/blue.gif)

<span data-ttu-id="f62e3-469">Blue = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="f62e3-469">Blue = "\#0000FF"</span></span>

![Exemplo de cor roxa.](images/purple.gif)

<span data-ttu-id="f62e3-471">Roxo = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="f62e3-471">Purple = "\#800080"</span></span>

![Exemplo de cor azul-petróleo.](images/teal.gif)

<span data-ttu-id="f62e3-473">Azul-petróleo = " \# 008080"</span><span class="sxs-lookup"><span data-stu-id="f62e3-473">Teal = "\#008080"</span></span>

![Exemplo de cor de Fuchsia.](images/fuchsia.gif)

<span data-ttu-id="f62e3-475">Fuchsia = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="f62e3-475">Fuchsia = "\#FF00FF"</span></span>

![Exemplo de cor de azul-piscina.](images/aqua.gif)

<span data-ttu-id="f62e3-477">Azul-piscina = " \# 00ffff"</span><span class="sxs-lookup"><span data-stu-id="f62e3-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="f62e3-478">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="f62e3-479">Cores do esquema</span><span class="sxs-lookup"><span data-stu-id="f62e3-479">Scheme colors</span></span>

<span data-ttu-id="f62e3-480">As cores do esquema referenciadas pelo esquema são definidas no nível do documento usando a marca meta com um atributo Name de "esquema de cores do tema".</span><span class="sxs-lookup"><span data-stu-id="f62e3-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="f62e3-481">Essa marca permite que até oito cores de esquema sejam definidas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="f62e3-482">As cores indefinidas devem padronizar para preto.</span><span class="sxs-lookup"><span data-stu-id="f62e3-482">Undefined colors should default to black.</span></span> <span data-ttu-id="f62e3-483">As cores do esquema permitem que o esquema de cores usado para um documento completo seja alterado apenas alterando o conteúdo do esquema de cores do tema.</span><span class="sxs-lookup"><span data-stu-id="f62e3-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="f62e3-484">Para garantir que os gráficos importados de diferentes aplicativos de criação façam uso consistente das cores do esquema, as seguintes interpretações são definidas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="f62e3-485">O "uso" é uma breve descrição da finalidade e a coluna "Descrição" fornece detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="f62e3-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="f62e3-486">Índice</span><span class="sxs-lookup"><span data-stu-id="f62e3-486">Index</span></span> | <span data-ttu-id="f62e3-487">Nome</span><span class="sxs-lookup"><span data-stu-id="f62e3-487">Name</span></span>              | <span data-ttu-id="f62e3-488">Uso</span><span class="sxs-lookup"><span data-stu-id="f62e3-488">Usage</span></span>                         | <span data-ttu-id="f62e3-489">Descrição</span><span class="sxs-lookup"><span data-stu-id="f62e3-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62e3-490">0</span><span class="sxs-lookup"><span data-stu-id="f62e3-490">0</span></span>     | <span data-ttu-id="f62e3-491">esquema. plano de fundo</span><span class="sxs-lookup"><span data-stu-id="f62e3-491">scheme.background</span></span> | <span data-ttu-id="f62e3-492">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="f62e3-492">Background</span></span>                    | <span data-ttu-id="f62e3-493">A cor usada para o plano de fundo de um elemento gráfico (e, frequentemente, para a página inteira).</span><span class="sxs-lookup"><span data-stu-id="f62e3-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="f62e3-494">1</span><span class="sxs-lookup"><span data-stu-id="f62e3-494">1</span></span>     | <span data-ttu-id="f62e3-495">esquema. texto</span><span class="sxs-lookup"><span data-stu-id="f62e3-495">scheme.text</span></span>       | <span data-ttu-id="f62e3-496">Texto e linhas</span><span class="sxs-lookup"><span data-stu-id="f62e3-496">Text and lines</span></span>                | <span data-ttu-id="f62e3-497">A cor do texto anexado a uma forma e a cor da linha padrão.</span><span class="sxs-lookup"><span data-stu-id="f62e3-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="f62e3-498">2</span><span class="sxs-lookup"><span data-stu-id="f62e3-498">2</span></span>     | <span data-ttu-id="f62e3-499">esquema. sombra</span><span class="sxs-lookup"><span data-stu-id="f62e3-499">scheme.shadow</span></span>     | <span data-ttu-id="f62e3-500">Sombras</span><span class="sxs-lookup"><span data-stu-id="f62e3-500">Shadows</span></span>                       | <span data-ttu-id="f62e3-501">Cor de sombra padrão – a cor normalmente usada para sombras de formas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="f62e3-502">3</span><span class="sxs-lookup"><span data-stu-id="f62e3-502">3</span></span>     | <span data-ttu-id="f62e3-503">esquema. title</span><span class="sxs-lookup"><span data-stu-id="f62e3-503">scheme.title</span></span>      | <span data-ttu-id="f62e3-504">Texto do título</span><span class="sxs-lookup"><span data-stu-id="f62e3-504">Title text</span></span>                    | <span data-ttu-id="f62e3-505">A cor a ser usada para o texto de título ou título.</span><span class="sxs-lookup"><span data-stu-id="f62e3-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="f62e3-506">4</span><span class="sxs-lookup"><span data-stu-id="f62e3-506">4</span></span>     | <span data-ttu-id="f62e3-507">esquema. Fill</span><span class="sxs-lookup"><span data-stu-id="f62e3-507">scheme.fill</span></span>       | <span data-ttu-id="f62e3-508">Esgota</span><span class="sxs-lookup"><span data-stu-id="f62e3-508">Fills</span></span>                         | <span data-ttu-id="f62e3-509">Cor de preenchimento padrão – a cor normalmente usada para preencher formas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="f62e3-510">5</span><span class="sxs-lookup"><span data-stu-id="f62e3-510">5</span></span>     | <span data-ttu-id="f62e3-511">esquema. acentuação</span><span class="sxs-lookup"><span data-stu-id="f62e3-511">scheme.accent</span></span>     | <span data-ttu-id="f62e3-512">Ênfase</span><span class="sxs-lookup"><span data-stu-id="f62e3-512">Accent</span></span>                        | <span data-ttu-id="f62e3-513">Cor normal de "Realce" usada para enfatizar um elemento importante de um elemento gráfico.</span><span class="sxs-lookup"><span data-stu-id="f62e3-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="f62e3-514">6</span><span class="sxs-lookup"><span data-stu-id="f62e3-514">6</span></span>     | <span data-ttu-id="f62e3-515">esquema. Hyperlink</span><span class="sxs-lookup"><span data-stu-id="f62e3-515">scheme.hyperlink</span></span>  | <span data-ttu-id="f62e3-516">Acento e hiperlink</span><span class="sxs-lookup"><span data-stu-id="f62e3-516">Accent and hyperlink</span></span>          | <span data-ttu-id="f62e3-517">Cor de realce usada para hiperlinks.</span><span class="sxs-lookup"><span data-stu-id="f62e3-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="f62e3-518">Pode ser usado para outras finalidades em que a cor denota um link para outras informações.</span><span class="sxs-lookup"><span data-stu-id="f62e3-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="f62e3-519">7</span><span class="sxs-lookup"><span data-stu-id="f62e3-519">7</span></span>     | <span data-ttu-id="f62e3-520">esquema. seguido</span><span class="sxs-lookup"><span data-stu-id="f62e3-520">scheme.followed</span></span>   | <span data-ttu-id="f62e3-521">Acento e hiperlink seguido</span><span class="sxs-lookup"><span data-stu-id="f62e3-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="f62e3-522">Cor de realce para hiperlinks seguidos; também apropriado para links "versões anteriores".</span><span class="sxs-lookup"><span data-stu-id="f62e3-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="f62e3-523">Uma cor de esquema pode ser referenciada por nome ou por índice, portanto, esquema. Fill e Scheme (4) são a mesma cor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="f62e3-524">As cores do esquema não participarão do esquema padrão se uma cor não for especificada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="f62e3-525">Uma cor de preenchimento não especificada sempre deve ser interpretada como branca, independentemente da cor da cor do esquema 4.</span><span class="sxs-lookup"><span data-stu-id="f62e3-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="f62e3-526">As cores de "destaque" devem ser iguais às cores do plano de fundo (0) e do preenchimento (4), e as cores do texto e do título devem ter a mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="f62e3-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="f62e3-527">Uma técnica padrão é fazer com que os acentos sejam coloridos e o texto padrão não seja colorido (normalmente preto ou branco).</span><span class="sxs-lookup"><span data-stu-id="f62e3-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="f62e3-528">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="f62e3-529">Cores do sistema</span><span class="sxs-lookup"><span data-stu-id="f62e3-529">System colors</span></span>

<span data-ttu-id="f62e3-530">Às vezes, os aplicativos registram cores com base nas configurações do sistema operacional em gráficos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="f62e3-531">Normalmente, eles são transitórios e não precisam ser gravados; as definições de thesystemcolor existem exclusivamente para dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="f62e3-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="f62e3-532">Uma cor do sistema é introduzida definindo uma marca apropriada em um novo namespace e inserindo as informações apropriadas no conteúdo do elemento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="f62e3-533">Essa proposta define tal marca para codificar as cores da interface do usuário do Windows definidas no arquivo de cabeçalho WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="f62e3-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="f62e3-534">O conteúdo do elemento é um único inteiro que contém o valor da cor relevante \_ definida de WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="f62e3-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="f62e3-535">Uma técnica semelhante pode ser adotada para qualquer especificação de cor específica do sistema ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="f62e3-536">É altamente recomendável que esse recurso seja usado apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f62e3-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="f62e3-537">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="f62e3-538">Cores puras</span><span class="sxs-lookup"><span data-stu-id="f62e3-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="f62e3-539">Se o elemento <pure/> aparecer em um valor de cor, será uma dica de que a cor não deve ser aproximada por um padrão de pontilhamento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="f62e3-540">Esse é um recurso de nível 1, e uma implementação de conformidade não precisa atendê-lo.</span><span class="sxs-lookup"><span data-stu-id="f62e3-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="f62e3-541">A designação é importante para os gráficos exibidos em dispositivos de alta resolução, como vídeos de vídeo, em que os pequenos recursos (como linhas) podem causar alias inadequado com cores diexistentes.</span><span class="sxs-lookup"><span data-stu-id="f62e3-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="f62e3-542">Em dispositivos como impressoras, que normalmente pontilham todas as cores, exceto para as poucas cores totalmente saturadas, o pontilhado normalmente é suficientemente bom para evitar esse problema.</span><span class="sxs-lookup"><span data-stu-id="f62e3-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="f62e3-543">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="f62e3-544">Ajustes de cores</span><span class="sxs-lookup"><span data-stu-id="f62e3-544">Color adjustments</span></span>

<span data-ttu-id="f62e3-545">A cor base pode ser ajustada por operações aritméticas no valor RGB.</span><span class="sxs-lookup"><span data-stu-id="f62e3-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="f62e3-546">Essas operações são definidas usando elementos adicionais dentro do valor de cor.</span><span class="sxs-lookup"><span data-stu-id="f62e3-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="f62e3-547">Esses ajustes são úteis somente quando aplicados a cores derivadas de outros elementos.</span><span class="sxs-lookup"><span data-stu-id="f62e3-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="f62e3-548">É válido especificar um ajuste desse tipo em um valor de cor fixo; no entanto, uma implementação tem permissão para reduzir isso para o valor RGB correspondente e armazená-lo em vez do original.</span><span class="sxs-lookup"><span data-stu-id="f62e3-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="f62e3-549">Todos os recursos de ajuste de cores descritos nesta seção são recursos de nível 1.</span><span class="sxs-lookup"><span data-stu-id="f62e3-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="f62e3-550">O parâmetro das seis primeiras operações é um único valor numérico integral no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="f62e3-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="f62e3-551">O ajuste é executado no valor de 3x8bit RGB da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f62e3-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="f62e3-552">Se <gray/> for especificado, o valor RGB será substituído por yyy, em que y é o valor de luminescência (y ") calculado a partir do valor sRGB no seguinte do ITU-r BT. 709.</span><span class="sxs-lookup"><span data-stu-id="f62e3-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="f62e3-553">Esse cálculo é:</span><span class="sxs-lookup"><span data-stu-id="f62e3-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="f62e3-554">Se uma modificação de Color. op for fornecida, cada componente será ajustado separadamente de acordo com a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f62e3-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="f62e3-555">c é o valor do componente e p é o valor Color. Parameter.</span><span class="sxs-lookup"><span data-stu-id="f62e3-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="f62e3-556">Operação</span><span class="sxs-lookup"><span data-stu-id="f62e3-556">Operation</span></span>       | <span data-ttu-id="f62e3-557">Fórmula</span><span class="sxs-lookup"><span data-stu-id="f62e3-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="f62e3-558">escureça</span><span class="sxs-lookup"><span data-stu-id="f62e3-558">darken</span></span>          | <span data-ttu-id="f62e3-559">c: = CXP/255</span><span class="sxs-lookup"><span data-stu-id="f62e3-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="f62e3-560">clarea</span><span class="sxs-lookup"><span data-stu-id="f62e3-560">lighten</span></span>         | <span data-ttu-id="f62e3-561">c: = 255-(255-c) XP/255</span><span class="sxs-lookup"><span data-stu-id="f62e3-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="f62e3-562">add</span><span class="sxs-lookup"><span data-stu-id="f62e3-562">add</span></span>             | <span data-ttu-id="f62e3-563">c: = c + p</span><span class="sxs-lookup"><span data-stu-id="f62e3-563">c := c + p</span></span>                         |
    | <span data-ttu-id="f62e3-564">subtrair</span><span class="sxs-lookup"><span data-stu-id="f62e3-564">subtract</span></span>        | <span data-ttu-id="f62e3-565">c: = c-p</span><span class="sxs-lookup"><span data-stu-id="f62e3-565">c := c - p</span></span>                         |
    | <span data-ttu-id="f62e3-566">reversesubtract</span><span class="sxs-lookup"><span data-stu-id="f62e3-566">reversesubtract</span></span> | <span data-ttu-id="f62e3-567">c: = p-c</span><span class="sxs-lookup"><span data-stu-id="f62e3-567">c := p - c</span></span>                         |
    | <span data-ttu-id="f62e3-568">blackwhite</span><span class="sxs-lookup"><span data-stu-id="f62e3-568">blackwhite</span></span>      | <span data-ttu-id="f62e3-569">se c < p thenc: = 0elsec: = 255</span><span class="sxs-lookup"><span data-stu-id="f62e3-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="f62e3-570">Em cada caso, se o valor do componente calculado, c, exceder 255, 255 será usado e, se for menor que 0, será usado 0.</span><span class="sxs-lookup"><span data-stu-id="f62e3-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="f62e3-571">Se <INVERT128/> for fornecido, o valor 128 será subtraído ou adicionado a cada componente de acordo com se o componente é menor que 128 ou não.</span><span class="sxs-lookup"><span data-stu-id="f62e3-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="f62e3-572">Se <invert/> for fornecido, cada componente será substituído por 255 menos o valor do componente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="f62e3-573">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="f62e3-574">la</span><span class="sxs-lookup"><span data-stu-id="f62e3-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="f62e3-575">Uma fonte é identificada usando um atributo Style, conforme definido na [seção CSS1 5,2 (Propriedades da fonte)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span><span class="sxs-lookup"><span data-stu-id="f62e3-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="f62e3-576">O corpo do elemento font é, no momento, indefinido, mas pode ser usado no futuro para codificar informações de fonte padrão.</span><span class="sxs-lookup"><span data-stu-id="f62e3-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="f62e3-577">As implementações iniciais dessa proposta devem preservar, mas não interpretar as informações.</span><span class="sxs-lookup"><span data-stu-id="f62e3-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="f62e3-578">É possível que o suporte seja adicionado no futuro para informações sobre fontes fora de linha (fontes para download ou recursos de fontes compartilhadas).</span><span class="sxs-lookup"><span data-stu-id="f62e3-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="f62e3-579">Isso será feito por um elemento de link de XML dentro do conteúdo do elemento font, garantindo compatbility para trás com implementações iniciais.</span><span class="sxs-lookup"><span data-stu-id="f62e3-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="f62e3-580">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="f62e3-581">bitmap</span><span class="sxs-lookup"><span data-stu-id="f62e3-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="f62e3-582">O elemento bitmap permite uma referência a um recurso de imagem fora de linha (normalmente um bitmap) a ser incluído em um gráfico.</span><span class="sxs-lookup"><span data-stu-id="f62e3-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="f62e3-583">bitmap é um recurso de nível 1.</span><span class="sxs-lookup"><span data-stu-id="f62e3-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="f62e3-584">O atributo de comportamento pode ser usado para indicar como o bitmap deve ser tratado por um aplicativo de edição.</span><span class="sxs-lookup"><span data-stu-id="f62e3-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="f62e3-585">O valor pode ser um ou ambos os tokens a seguir.</span><span class="sxs-lookup"><span data-stu-id="f62e3-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="f62e3-586">Token</span><span class="sxs-lookup"><span data-stu-id="f62e3-586">Token</span></span>    | <span data-ttu-id="f62e3-587">Descrição</span><span class="sxs-lookup"><span data-stu-id="f62e3-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62e3-588">separado</span><span class="sxs-lookup"><span data-stu-id="f62e3-588">separate</span></span> | <span data-ttu-id="f62e3-589">Marca o bitmap como uma entidade separada, que não deve ser considerada como parte integral do documento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="f62e3-590">O bitmap não deve ser mantido com o documento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="f62e3-591">Se o documento for copiado, o bitmap não deverá ser copiado; Se o documento for movido, o bitmap não deverá ser movido com ele.</span><span class="sxs-lookup"><span data-stu-id="f62e3-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="f62e3-592">original</span><span class="sxs-lookup"><span data-stu-id="f62e3-592">original</span></span> | <span data-ttu-id="f62e3-593">O atributo title identifica o local original do bitmap como uma URL; caso contrário, o significado do título não será especificado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="f62e3-594">Esses valores são dicas para o comportamento esperado.</span><span class="sxs-lookup"><span data-stu-id="f62e3-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="f62e3-595">A opção separada refere-se ao comportamento dos dados referenciados por href.</span><span class="sxs-lookup"><span data-stu-id="f62e3-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="f62e3-596">Se o separado e o original forem fornecidos, o aplicativo deverá desconsiderar o URI href e regenerar o bitmap a partir dos dados originais.</span><span class="sxs-lookup"><span data-stu-id="f62e3-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="f62e3-597">Se apenas o original for fornecido, o aplicativo deverá usar o URI href para localizar o bitmap, mas poderá dar ao usuário a opção de gerá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="f62e3-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="f62e3-598">É válido fazer com que o URI href e o atributo title tenham o mesmo valor (léxico) – isso é apropriado se o bitmap referenciado não for "armazenado com" o documento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="f62e3-599">Ele é destinado (embora não necessário) que href seja usado para a própria cópia do documento do bitmap, que pode ser excluído se as formas de referência forem excluídas--e esse título for usado para indicar uma cópia compartilhada.</span><span class="sxs-lookup"><span data-stu-id="f62e3-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="f62e3-600">Portanto, se ambos contiverem o mesmo valor, não haverá cópia específica do documento.</span><span class="sxs-lookup"><span data-stu-id="f62e3-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="f62e3-601">Os aplicativos podem desconsiderar a dica se não couber com o modelo de armazenamento real dos dados XML.</span><span class="sxs-lookup"><span data-stu-id="f62e3-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="f62e3-602">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="f62e3-603">Formatos de arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="f62e3-603">Picture file formats</span></span>

<span data-ttu-id="f62e3-604">Dentro do contexto dessa proposta, os dados externos são invariavelmente um bitmap ou um arquivo que é usado para produzir um bitmap.</span><span class="sxs-lookup"><span data-stu-id="f62e3-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="f62e3-605">No nível de renderização 0, nenhum formato de bitmap externo precisa ser suportado-os caminhos só podem ser preenchidos com cores sólidas.</span><span class="sxs-lookup"><span data-stu-id="f62e3-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="f62e3-606">Para renderizar o conjunto completo de preenchimentos de nível 1 de renderização, os bitmaps precisam ter suporte.</span><span class="sxs-lookup"><span data-stu-id="f62e3-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="f62e3-607">O nível de renderização 1 inclui (apenas) os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="f62e3-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="f62e3-608">JFIF, ou seja, dados de formato ISO/IEC 10918 inseridos em um arquivo com o cabeçalho JFIF (que pode ser considerado um marcador APP0 específico após o SOI Maker) e incluindo (somente) o intervalo de formatos JPEG com suporte no código V6 IJG.</span><span class="sxs-lookup"><span data-stu-id="f62e3-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="f62e3-609">PNG, conforme definido pela especificação do PNG versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="f62e3-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="f62e3-610">O nível de renderização 2 também inclui suporte para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f62e3-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="f62e3-611">GIF, conforme definido pela especificação GIF publicada por CompuServ em 1987 (normalmente chamado de "GIF87a").</span><span class="sxs-lookup"><span data-stu-id="f62e3-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="f62e3-612">GIF89a também deve ter suporte nesse nível, sujeito à restrição de que os dados não devem conter nenhum bloco de extensão que precise de interpretação para exibir o bitmap diferente do requisito de extensionswithouta de controle de gráficos para a entrada do usuário ou um tempo de atraso.</span><span class="sxs-lookup"><span data-stu-id="f62e3-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="f62e3-613">Isso permite que os comentários sejam incluídos, mas não a extensão de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="f62e3-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="f62e3-614">Um aplicativo pode inserir extensões de aplicativo (0x21, 0xFF), mas, usando a terminologia desta proposta, elas devem conter apenas os dados de edição, não de renderização.</span><span class="sxs-lookup"><span data-stu-id="f62e3-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="f62e3-615">Qualquer outro formato de dados usado no gráfico força esse gráfico a ser pelo menos o nível 3 de edição e, possivelmente, o nível 3 de renderização (se os dados forem necessários para renderizar o gráfico).</span><span class="sxs-lookup"><span data-stu-id="f62e3-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="f62e3-616">Um aplicativo é incentivado a publicar os formatos que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="f62e3-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="f62e3-617">Por exemplo, Microsoft Office dá suporte aos seguintes formatos adicionais nativamente e, portanto, pode gravar dados de edição neste formulário:</span><span class="sxs-lookup"><span data-stu-id="f62e3-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="f62e3-618">WMF--metarquivo do Windows (formato Win 3,1)</span><span class="sxs-lookup"><span data-stu-id="f62e3-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="f62e3-619">EMF--metarquivo "avançado" do Windows (formato Win32)</span><span class="sxs-lookup"><span data-stu-id="f62e3-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="f62e3-620">PICT--Mac OS arquivo QuickDraw PICT (todas as versões, mas sem registros QuickTime ou outras extensões)</span><span class="sxs-lookup"><span data-stu-id="f62e3-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="f62e3-621">BMP--formato de arquivo de bitmap do Windows, formatos "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 e BITMAPV5</span><span class="sxs-lookup"><span data-stu-id="f62e3-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="f62e3-622">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f62e3-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="f62e3-623">vector</span><span class="sxs-lookup"><span data-stu-id="f62e3-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="f62e3-624">Um caminho gráfico vetorial é codificado como PCDATA.</span><span class="sxs-lookup"><span data-stu-id="f62e3-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="f62e3-625">O conteúdo do elemento v é misto, contendo uma descrição de caminho de vetor opcionalmente parametrizada com elementos p.</span><span class="sxs-lookup"><span data-stu-id="f62e3-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="f62e3-626">Voltar para a visão geral da VML</span><span class="sxs-lookup"><span data-stu-id="f62e3-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

