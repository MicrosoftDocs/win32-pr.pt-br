---
title: Efeito de turbulência
description: Use o efeito turbulência para gerar um bitmap com base na função de ruído Perl.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- efeito de turbulência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566541"
---
# <a name="turbulence-effect"></a><span data-ttu-id="40c7f-104">Efeito de turbulência</span><span class="sxs-lookup"><span data-stu-id="40c7f-104">Turbulence effect</span></span>

<span data-ttu-id="40c7f-105">Use o efeito turbulência para gerar um bitmap com base na função de ruído Perl.</span><span class="sxs-lookup"><span data-stu-id="40c7f-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="40c7f-106">O efeito turbulência não tem nenhuma imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="40c7f-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="40c7f-107">O CLSID para esse efeito é CLSID \_ D2D1Turbulence.</span><span class="sxs-lookup"><span data-stu-id="40c7f-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="40c7f-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="40c7f-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="40c7f-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="40c7f-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="40c7f-110">Modos de ruído</span><span class="sxs-lookup"><span data-stu-id="40c7f-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="40c7f-111">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="40c7f-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="40c7f-112">Requirements</span><span class="sxs-lookup"><span data-stu-id="40c7f-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="40c7f-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40c7f-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="40c7f-114">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="40c7f-114">Example image</span></span>

![captura de tela de exemplo de efeito mostrando a saída do efeito turbulência.](images/32-turbulence.png)

<span data-ttu-id="40c7f-116">O efeito turbulência computa a soma de um ou mais octaves da função de ruído do Perlm.</span><span class="sxs-lookup"><span data-stu-id="40c7f-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="40c7f-117">O ruído de Perl é uma função pseudo aleatória cujo valor depende da frequência, da posição e do valor de semente.</span><span class="sxs-lookup"><span data-stu-id="40c7f-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="40c7f-118">O efeito gera os valores RGBA usando uma dessas equações.</span><span class="sxs-lookup"><span data-stu-id="40c7f-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="40c7f-119">Se você selecionar o modo de ruído de soma de ruído de D2D1 \_ turbulência, \_ \_ \_ o efeito usará essa equação.</span><span class="sxs-lookup"><span data-stu-id="40c7f-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![Captura de tela que mostra a função turbulência usada para gerar um bitmap.](images/turbulence-equation1.png)

<span data-ttu-id="40c7f-121">Se você selecionar o modo de ruído D2D1 \_ turbulência de \_ ruído \_ turbulência, o efeito usará essa equação.</span><span class="sxs-lookup"><span data-stu-id="40c7f-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![a função turbulência usada para gerar um bitmap.](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="40c7f-123">A `PerlinNoise` função tem um intervalo de \[ -1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="40c7f-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="40c7f-124">Esse efeito gera valores de pixel no alfa precalculado.</span><span class="sxs-lookup"><span data-stu-id="40c7f-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="40c7f-125">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="40c7f-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40c7f-126">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="40c7f-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="40c7f-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="40c7f-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40c7f-128">Deslocamento</span><span class="sxs-lookup"><span data-stu-id="40c7f-128">Offset</span></span><br/> <span data-ttu-id="40c7f-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="40c7f-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="40c7f-130">As coordenadas em que a saída turbulência é gerada.</span><span class="sxs-lookup"><span data-stu-id="40c7f-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="40c7f-131">O algoritmo usado para gerar o ruído de Perl é dependente da posição, portanto, um deslocamento diferente resulta em uma saída diferente.</span><span class="sxs-lookup"><span data-stu-id="40c7f-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="40c7f-132">Essa propriedade não está vinculada e as unidades são especificadas em DIPs</span><span class="sxs-lookup"><span data-stu-id="40c7f-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40c7f-133">O deslocamento não tem o mesmo efeito que uma tradução, pois a saída da função de ruído é infinita e a função será encodificada ao lado do bloco.</span><span class="sxs-lookup"><span data-stu-id="40c7f-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="40c7f-134">O tipo é D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="40c7f-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="40c7f-135">O valor padrão é {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="40c7f-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c7f-136">Tamanho</span><span class="sxs-lookup"><span data-stu-id="40c7f-136">Size</span></span><br/> <span data-ttu-id="40c7f-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="40c7f-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="40c7f-138">O tamanho da saída do turbulência.</span><span class="sxs-lookup"><span data-stu-id="40c7f-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="40c7f-139">Essa propriedade não está vinculada e as unidades são especificadas em DIPs</span><span class="sxs-lookup"><span data-stu-id="40c7f-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="40c7f-140">O tipo é D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="40c7f-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="40c7f-141">O valor padrão é {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="40c7f-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c7f-142">BaseFrequency</span><span class="sxs-lookup"><span data-stu-id="40c7f-142">BaseFrequency</span></span><br/> <span data-ttu-id="40c7f-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="40c7f-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="40c7f-144">As frequências de base nas direções X e Y.</span><span class="sxs-lookup"><span data-stu-id="40c7f-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="40c7f-145">Esta propriedade é um float e deve ser maior que 0.</span><span class="sxs-lookup"><span data-stu-id="40c7f-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="40c7f-146">As unidades são especificadas em 1/DIPs.</span><span class="sxs-lookup"><span data-stu-id="40c7f-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="40c7f-147">Um valor de 1 (1/DIPs) para a frequência base resulta no ruído de Perl, concluindo um ciclo inteiro entre dois pixels.</span><span class="sxs-lookup"><span data-stu-id="40c7f-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="40c7f-148">A interpolação de atenuação para esses pixels resulta em pixels completamente aleatórios, já que não há nenhuma correlação entre os pixels.</span><span class="sxs-lookup"><span data-stu-id="40c7f-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="40c7f-149">Um valor de 0,1 (1/DIPs) para a frequência base, a função de ruído de Perlm se repete a cada 10 DIPs.</span><span class="sxs-lookup"><span data-stu-id="40c7f-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="40c7f-150">Isso resulta em uma correlação entre pixels e o efeito típico de turbulência é visível.</span><span class="sxs-lookup"><span data-stu-id="40c7f-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="40c7f-151">O tipo é D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="40c7f-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="40c7f-152">O valor padrão é {0,01 f, 0,01 f}.</span><span class="sxs-lookup"><span data-stu-id="40c7f-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c7f-153">NumOctaves</span><span class="sxs-lookup"><span data-stu-id="40c7f-153">NumOctaves</span></span><br/> <span data-ttu-id="40c7f-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="40c7f-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="40c7f-155">O número de octaves para a função de ruído.</span><span class="sxs-lookup"><span data-stu-id="40c7f-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="40c7f-156">Esta propriedade é um UINT32 e deve ser maior que 0.</span><span class="sxs-lookup"><span data-stu-id="40c7f-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="40c7f-157">O tipo é UINT32.</span><span class="sxs-lookup"><span data-stu-id="40c7f-157">The type is UINT32.</span></span><br/> <span data-ttu-id="40c7f-158">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="40c7f-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c7f-159">Seed</span><span class="sxs-lookup"><span data-stu-id="40c7f-159">Seed</span></span><br/> <span data-ttu-id="40c7f-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="40c7f-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="40c7f-161">A semente do gerador de pseudo aleatório.</span><span class="sxs-lookup"><span data-stu-id="40c7f-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="40c7f-162">Esta propriedade não está associada.</span><span class="sxs-lookup"><span data-stu-id="40c7f-162">This property is unbounded.</span></span><br/> <span data-ttu-id="40c7f-163">O tipo é UINT32.</span><span class="sxs-lookup"><span data-stu-id="40c7f-163">The type is UINT32.</span></span><br/> <span data-ttu-id="40c7f-164">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="40c7f-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c7f-165">Ruído</span><span class="sxs-lookup"><span data-stu-id="40c7f-165">Noise</span></span><br/> <span data-ttu-id="40c7f-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="40c7f-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="40c7f-167">O modo de ruído turbulência.</span><span class="sxs-lookup"><span data-stu-id="40c7f-167">The turbulence noise mode.</span></span> <span data-ttu-id="40c7f-168">Essa propriedade pode ser <em>fractal Sum</em> ou <em>turbulência</em>.</span><span class="sxs-lookup"><span data-stu-id="40c7f-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="40c7f-169">Indica se um bitmap deve ser gerado com base no ruído de fractal ou na função turbulência.</span><span class="sxs-lookup"><span data-stu-id="40c7f-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="40c7f-170">Consulte <a href="#noise-modes">modos de ruído</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="40c7f-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="40c7f-171">O tipo é D2D1_TURBULENCE_NOISE.</span><span class="sxs-lookup"><span data-stu-id="40c7f-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="40c7f-172">O valor padrão é D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span><span class="sxs-lookup"><span data-stu-id="40c7f-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c7f-173">Costura</span><span class="sxs-lookup"><span data-stu-id="40c7f-173">Stitchable</span></span><br/> <span data-ttu-id="40c7f-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="40c7f-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="40c7f-175">Ativa ou desativa o grampeamento.</span><span class="sxs-lookup"><span data-stu-id="40c7f-175">Turns stitching on or off.</span></span> <span data-ttu-id="40c7f-176">A frequência base é ajustada para que o bitmap de saída possa ser grampeado.</span><span class="sxs-lookup"><span data-stu-id="40c7f-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="40c7f-177">Isso será útil se você quiser dividir várias cópias da saída do efeito turbulência.</span><span class="sxs-lookup"><span data-stu-id="40c7f-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="40c7f-178">True o bitmap de saída pode ser enquadrado (usando o efeito de bloco) sem a aparência de emendas.</span><span class="sxs-lookup"><span data-stu-id="40c7f-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="40c7f-179">A frequência base é ajustada para que o bitmap de saída possa ser grampeado.</span><span class="sxs-lookup"><span data-stu-id="40c7f-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="40c7f-180">False a frequência base não é ajustada, portanto, as fendas podem aparecer entre os blocos se o bitmap for enlado.</span><span class="sxs-lookup"><span data-stu-id="40c7f-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="40c7f-181">O tipo é BOOL.</span><span class="sxs-lookup"><span data-stu-id="40c7f-181">The type is BOOL.</span></span><br/> <span data-ttu-id="40c7f-182">O valor padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="40c7f-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="40c7f-183">Modos de ruído</span><span class="sxs-lookup"><span data-stu-id="40c7f-183">Noise modes</span></span>



| <span data-ttu-id="40c7f-184">Enumeração</span><span class="sxs-lookup"><span data-stu-id="40c7f-184">Enumeration</span></span>                           | <span data-ttu-id="40c7f-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="40c7f-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40c7f-186">\_Soma de \_ fractal de ruído d2d1 turbulência \_ \_</span><span class="sxs-lookup"><span data-stu-id="40c7f-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="40c7f-187">Computa uma soma do octaves, deslocando o intervalo de saída de \[ -1, 1 \] , para \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="40c7f-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="40c7f-188">D2D1 \_ turbulência \_ Noise \_ turbulência</span><span class="sxs-lookup"><span data-stu-id="40c7f-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="40c7f-189">Computa uma soma do valor absoluto de cada Octave.</span><span class="sxs-lookup"><span data-stu-id="40c7f-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="40c7f-190">Nenhum modo contém um fixe explícito dos valores de saída.</span><span class="sxs-lookup"><span data-stu-id="40c7f-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="40c7f-191">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="40c7f-191">Output bitmap</span></span>

<span data-ttu-id="40c7f-192">Esse efeito gera um bitmap de tamanho logicamente infinito.</span><span class="sxs-lookup"><span data-stu-id="40c7f-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c7f-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40c7f-193">Requirements</span></span>



| <span data-ttu-id="40c7f-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="40c7f-194">Requirement</span></span> | <span data-ttu-id="40c7f-195">Valor</span><span class="sxs-lookup"><span data-stu-id="40c7f-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40c7f-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c7f-196">Minimum supported client</span></span> | <span data-ttu-id="40c7f-197">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="40c7f-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="40c7f-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c7f-198">Minimum supported server</span></span> | <span data-ttu-id="40c7f-199">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="40c7f-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="40c7f-200">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40c7f-200">Header</span></span>                   | <span data-ttu-id="40c7f-201">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="40c7f-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="40c7f-202">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40c7f-202">Library</span></span>                  | <span data-ttu-id="40c7f-203">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="40c7f-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="40c7f-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40c7f-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40c7f-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="40c7f-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

