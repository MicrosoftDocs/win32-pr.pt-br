---
title: Efeito de mesclagem
description: Use o efeito de mistura para combinar 2 imagens. Esse efeito tem 26 modos de mesclagem.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- efeito de mistura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824743"
---
# <a name="blend-effect"></a><span data-ttu-id="01a1e-105">Efeito de mesclagem</span><span class="sxs-lookup"><span data-stu-id="01a1e-105">Blend effect</span></span>

<span data-ttu-id="01a1e-106">Use o efeito de mistura para combinar 2 imagens.</span><span class="sxs-lookup"><span data-stu-id="01a1e-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="01a1e-107">Esse efeito tem 26 modos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="01a1e-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="01a1e-108">O CLSID para esse efeito é CLSID \_ D2D1Blend.</span><span class="sxs-lookup"><span data-stu-id="01a1e-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="01a1e-109">Exemplos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="01a1e-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="01a1e-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="01a1e-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="01a1e-111">Modos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="01a1e-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="01a1e-112">Conversões de espaço de cores HSL</span><span class="sxs-lookup"><span data-stu-id="01a1e-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="01a1e-113">Convertendo de RGB em HSL</span><span class="sxs-lookup"><span data-stu-id="01a1e-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="01a1e-114">Convertendo de HSL para RGB</span><span class="sxs-lookup"><span data-stu-id="01a1e-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="01a1e-115">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="01a1e-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="01a1e-116">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="01a1e-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="01a1e-117">Requirements</span><span class="sxs-lookup"><span data-stu-id="01a1e-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="01a1e-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01a1e-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="01a1e-119">Exemplos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="01a1e-119">Blending examples</span></span>

<span data-ttu-id="01a1e-120">Aqui está uma imagem de exemplo de cada modo de mesclagem do efeito de mistura.</span><span class="sxs-lookup"><span data-stu-id="01a1e-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="01a1e-121">Uma lista completa dos modos de mesclagem e as propriedades do modo correspondente estão na próxima seção</span><span class="sxs-lookup"><span data-stu-id="01a1e-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![captura de tela de exemplo de efeito de todos os modos de mistura disponíveis.](images/blend-modes.png)

<span data-ttu-id="01a1e-123">Aqui está outro exemplo que usa o modo de exclusão.</span><span class="sxs-lookup"><span data-stu-id="01a1e-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="01a1e-124">Antes da imagem 1</span><span class="sxs-lookup"><span data-stu-id="01a1e-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg)    |
| <span data-ttu-id="01a1e-126">Antes da imagem 2</span><span class="sxs-lookup"><span data-stu-id="01a1e-126">Before image 2</span></span>                                                             |
| ![a segunda imagem antes do efeito.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="01a1e-128">After (após)</span><span class="sxs-lookup"><span data-stu-id="01a1e-128">After</span></span>                                                                      |
| ![a imagem após a transformação.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="01a1e-130">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="01a1e-130">Effect properties</span></span>



| <span data-ttu-id="01a1e-131">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="01a1e-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="01a1e-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="01a1e-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a1e-133">Mode</span><span class="sxs-lookup"><span data-stu-id="01a1e-133">Mode</span></span><br/> <span data-ttu-id="01a1e-134">\_Modo de \_ prop d2d1 Blend \_</span><span class="sxs-lookup"><span data-stu-id="01a1e-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="01a1e-135">O modo de mesclagem usado para o efeito.</span><span class="sxs-lookup"><span data-stu-id="01a1e-135">The blend mode used for the effect.</span></span> <span data-ttu-id="01a1e-136">Consulte [modos de mesclagem](#blend-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="01a1e-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="01a1e-137">O tipo é o \_ modo de mesclagem d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="01a1e-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="01a1e-138">O valor padrão é \_ multiplicar modo de mesclagem d2d1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="01a1e-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="01a1e-139">Modos do Blend</span><span class="sxs-lookup"><span data-stu-id="01a1e-139">Blend modes</span></span>

<span data-ttu-id="01a1e-140">A tabela aqui mostra todos os modos de mesclagem desse efeito.</span><span class="sxs-lookup"><span data-stu-id="01a1e-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="01a1e-141">As funções auxiliares necessárias para computar a saída do efeito estão na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="01a1e-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="01a1e-142">Cor: O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>A</sub>) + B <sub>RGB</sub> \* B <sub>a</sub> \* (1-f <sub>a</sub>)</span><span class="sxs-lookup"><span data-stu-id="01a1e-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="01a1e-143">Alfa: O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>A</sub>) + B<sub>A</sub></span><span class="sxs-lookup"><span data-stu-id="01a1e-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="01a1e-144">Em que:</span><span class="sxs-lookup"><span data-stu-id="01a1e-144">Where:</span></span>

-   <span data-ttu-id="01a1e-145">O<sub>PRGB</sub> é a cor de saída previamente multiplicada</span><span class="sxs-lookup"><span data-stu-id="01a1e-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="01a1e-146">O<sub>A</sub> é Alfa de saída</span><span class="sxs-lookup"><span data-stu-id="01a1e-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="01a1e-147">B<sub>RGB</sub> é a cor de destino não multiplicada previamente</span><span class="sxs-lookup"><span data-stu-id="01a1e-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="01a1e-148">B<sub>A é o</sub> destino alfa</span><span class="sxs-lookup"><span data-stu-id="01a1e-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="01a1e-149">F<sub>RGB</sub> é a cor de origem não multiplicada previamente</span><span class="sxs-lookup"><span data-stu-id="01a1e-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="01a1e-150">F<sub>A</sub> é fonte alfa</span><span class="sxs-lookup"><span data-stu-id="01a1e-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="01a1e-151">*f*(S <sub>RGB</sub>, D <sub>RGB</sub>) é uma função de mistura que varia de acordo com o modo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="01a1e-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="01a1e-152">Alguns dos modos de mesclagem exigem a conversão de e para o espaço de cores de matiz, saturação, luminosidade (HSL) para RGB.</span><span class="sxs-lookup"><span data-stu-id="01a1e-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01a1e-153">Enumeração</span><span class="sxs-lookup"><span data-stu-id="01a1e-153">Enumeration</span></span></th>
<th><span data-ttu-id="01a1e-154">Subscrito</span><span class="sxs-lookup"><span data-stu-id="01a1e-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01a1e-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="01a1e-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="01a1e-156">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="01a1e-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="01a1e-158">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="01a1e-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="01a1e-160">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="01a1e-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="01a1e-162">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="01a1e-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="01a1e-164">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="01a1e-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="01a1e-166">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="01a1e-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="01a1e-168">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="01a1e-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="01a1e-170">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="01a1e-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="01a1e-172">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="01a1e-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="01a1e-174">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="01a1e-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="01a1e-176">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="01a1e-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="01a1e-178">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="01a1e-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="01a1e-180">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="01a1e-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="01a1e-182">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="01a1e-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="01a1e-184">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="01a1e-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="01a1e-186">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="01a1e-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="01a1e-188">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="01a1e-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="01a1e-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="01a1e-190">Fórmulas de mesclagem básicas com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B<sub>RGB</sub>)</span><span class="sxs-lookup"><span data-stu-id="01a1e-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="01a1e-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="01a1e-192">Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RGB</sub>   2 \* f<sub>RGB</sub> \* B<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="01a1e-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="01a1e-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="01a1e-194">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="01a1e-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="01a1e-196">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="01a1e-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="01a1e-198">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="01a1e-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="01a1e-200">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="01a1e-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="01a1e-202">Considerando:</span><span class="sxs-lookup"><span data-stu-id="01a1e-202">Given:</span></span>
<ul>
<li><span data-ttu-id="01a1e-203">Uma coordenada de cena XY para o pixel atual</span><span class="sxs-lookup"><span data-stu-id="01a1e-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="01a1e-204">Um gerador de números pseudo aleatórios (XY) determinístico com base na coordenada de semente XY, com distribuição não polarizada de valores de [0, 1]</span><span class="sxs-lookup"><span data-stu-id="01a1e-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01a1e-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="01a1e-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="01a1e-206">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01a1e-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="01a1e-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="01a1e-208">Fórmula de mesclagem básica somente para alfa.</span><span class="sxs-lookup"><span data-stu-id="01a1e-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="01a1e-209">Para todos os modos de mesclagem, o valor de saída é premultiplicado e clamped para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="01a1e-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="01a1e-210">Conversões de espaço de cores HSL</span><span class="sxs-lookup"><span data-stu-id="01a1e-210">HSL color space conversions</span></span>

<span data-ttu-id="01a1e-211">O componente de luminosidade é calculado usando os pesos RGB aqui:</span><span class="sxs-lookup"><span data-stu-id="01a1e-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="01a1e-212">*k*<sub>R</sub> = 0,30</span><span class="sxs-lookup"><span data-stu-id="01a1e-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="01a1e-213">*k*<sub>G</sub> = 0,59</span><span class="sxs-lookup"><span data-stu-id="01a1e-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="01a1e-214">*k*<sub>B</sub> = 0,11</span><span class="sxs-lookup"><span data-stu-id="01a1e-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="01a1e-215">Convertendo de RGB em HSL</span><span class="sxs-lookup"><span data-stu-id="01a1e-215">Converting from RGB to HSL</span></span>

![fórmula matemática que descreve a transformação de cor RGB para cor HSL.](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="01a1e-217">Isso coloca *S* e *L* no intervalo de \[ 0,0, 1,0 \] e *H* no intervalo \[ -1,0, 5,0 \] .</span><span class="sxs-lookup"><span data-stu-id="01a1e-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="01a1e-218">Convertendo de HSL para RGB</span><span class="sxs-lookup"><span data-stu-id="01a1e-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="01a1e-219">Para converter a outra maneira, usamos o inverso dos cálculos anteriores.</span><span class="sxs-lookup"><span data-stu-id="01a1e-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="01a1e-220">Se *S* = 0, *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="01a1e-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="01a1e-221">Caso contrário, há seis casos dependentes de matiz:</span><span class="sxs-lookup"><span data-stu-id="01a1e-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="01a1e-222">Se *H* for maior que 0, os valores estarão no setor vermelho/magenta em que *R*  >  *B*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="01a1e-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![matemática equaiton etapa um dos seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="01a1e-224">Se *H* for maior ou igual a 0 e menor que 1, os valores estarão no setor vermelho/amarelo em que *R*  >  *G*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="01a1e-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![matemática equaiton etapa dois de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="01a1e-226">Se *H* for maior ou igual a 1 e menor que 2, os valores estarão no setor amarelo/verde em que *G*  >  *R*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="01a1e-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![matemática equaiton etapa três de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="01a1e-228">Se *H* for maior ou igual a 2 e menor que 3, os valores estarão no setor verde/ciano em que *G*  >  *B*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="01a1e-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![matemática equaiton etapa quatro de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="01a1e-230">Se *H* for maior ou igual a 3 e menor que 4, os valores estarão no setor ciano/azul em que *B*  >  *G*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="01a1e-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![matemática equaiton etapa cinco de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="01a1e-232">Se *H* for maior ou igual a 4, os valores estarão no setor azul/magenta em que *B*  >  *R*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="01a1e-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![matemática equaiton etapa seis de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="01a1e-234">Como os modos de mesclagem fazem combinações arbitrárias de componentes HSL de duas cores diferentes, é comum que o valor RGB convertido esteja fora de gama, ou seja, um ou mais componentes de canal possam estar fora do intervalo legal de \[ 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="01a1e-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="01a1e-235">Essas cores são revertidas de acordo com a redução mínima da saturação, preservando, ao mesmo tempo, a matiz e a luminosidade:</span><span class="sxs-lookup"><span data-stu-id="01a1e-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![fórmula matemática que descreve as correções necessárias para as instâncias fora de gamut.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="01a1e-237">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="01a1e-237">Output bitmap</span></span>

<span data-ttu-id="01a1e-238">O bitmap de saída para esse efeito é sempre o tamanho da União das duas imagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="01a1e-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="01a1e-239">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="01a1e-239">Sample code</span></span>

<span data-ttu-id="01a1e-240">Para obter um exemplo desse efeito, baixe o [exemplo de modos de efeito composto Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="01a1e-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="01a1e-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a1e-241">Requirements</span></span>



| <span data-ttu-id="01a1e-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a1e-242">Requirement</span></span> | <span data-ttu-id="01a1e-243">Valor</span><span class="sxs-lookup"><span data-stu-id="01a1e-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01a1e-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a1e-244">Minimum supported client</span></span> | <span data-ttu-id="01a1e-245">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="01a1e-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="01a1e-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a1e-246">Minimum supported server</span></span> | <span data-ttu-id="01a1e-247">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="01a1e-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="01a1e-248">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01a1e-248">Header</span></span>                   | <span data-ttu-id="01a1e-249">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="01a1e-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="01a1e-250">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01a1e-250">Library</span></span>                  | <span data-ttu-id="01a1e-251">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="01a1e-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="01a1e-252">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01a1e-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a1e-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="01a1e-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

