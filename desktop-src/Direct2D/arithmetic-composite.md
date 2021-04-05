---
title: Efeito composto aritmético
description: Use o efeito de composição aritmética para combinar 2 imagens usando uma soma ponderada de pixels das imagens de entrada.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- efeito composto aritmético
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918919"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="0cb44-104">Efeito composto aritmético</span><span class="sxs-lookup"><span data-stu-id="0cb44-104">Arithmetic composite effect</span></span>

<span data-ttu-id="0cb44-105">Use o efeito de composição aritmética para combinar 2 imagens usando uma soma ponderada de pixels das imagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="0cb44-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="0cb44-106">O CLSID para esse efeito é CLSID \_ D2D1ArithmeticComposite.</span><span class="sxs-lookup"><span data-stu-id="0cb44-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="0cb44-107">Fórmula</span><span class="sxs-lookup"><span data-stu-id="0cb44-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="0cb44-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="0cb44-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="0cb44-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="0cb44-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0cb44-110">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="0cb44-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="0cb44-111">Requirements</span><span class="sxs-lookup"><span data-stu-id="0cb44-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0cb44-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cb44-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="0cb44-113">Fórmula</span><span class="sxs-lookup"><span data-stu-id="0cb44-113">Formula</span></span>

<span data-ttu-id="0cb44-114">A fórmula aqui é usada para computar esse efeito.</span><span class="sxs-lookup"><span data-stu-id="0cb44-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="0cb44-115">Saída<sub>RGBA</sub> = destino \* de<sub>RGBA</sub> de origem de fonte de software \* <sub>RGBA</sub> + C2 \* origem<sub>RGBA</sub> + C3 \* Destination<sub>RGBA</sub> + C4</span><span class="sxs-lookup"><span data-stu-id="0cb44-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="0cb44-116">Onde C1, C2, C3, C4 são os coeficientes que você define.</span><span class="sxs-lookup"><span data-stu-id="0cb44-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="0cb44-117">Os coeficientes mapeiam os valores em um \_ vetor d2d1 \_ 4F (x, y, z, w):</span><span class="sxs-lookup"><span data-stu-id="0cb44-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="0cb44-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="0cb44-118">x = C1</span></span>
-   <span data-ttu-id="0cb44-119">y = C2</span><span class="sxs-lookup"><span data-stu-id="0cb44-119">y = C2</span></span>
-   <span data-ttu-id="0cb44-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="0cb44-120">z = C3</span></span>
-   <span data-ttu-id="0cb44-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="0cb44-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="0cb44-122">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="0cb44-122">Example image</span></span>

<span data-ttu-id="0cb44-123">Um exemplo simples é adicionar os pixels de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="0cb44-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="0cb44-124">No exemplo, 2 retângulos arredondados são compostos juntos.</span><span class="sxs-lookup"><span data-stu-id="0cb44-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="0cb44-125">O retângulo de origem é azul e o destino é vermelho.</span><span class="sxs-lookup"><span data-stu-id="0cb44-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="0cb44-126">A imagem aqui é a saída do efeito composto aritmético com os coeficientes da equação definida com os valores aqui.</span><span class="sxs-lookup"><span data-stu-id="0cb44-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="0cb44-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="0cb44-127">C1 = 0</span></span>
-   <span data-ttu-id="0cb44-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="0cb44-128">C2 = 1</span></span>
-   <span data-ttu-id="0cb44-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="0cb44-129">C3 = 1</span></span>
-   <span data-ttu-id="0cb44-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="0cb44-130">C4 = 0</span></span>

![uma imagem de exemplo mostrando dois retângulos arredondados do mesmo tamanho que se sobrepõem usando o efeito composto aritmético.](images/arithmetic-50-percent.png)

<span data-ttu-id="0cb44-132">O resultado é que os valores de pixel para a origem e o destino são adicionados.</span><span class="sxs-lookup"><span data-stu-id="0cb44-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="0cb44-133">As regiões onde os retângulos não se sobrepõem aos valores RGBA são todos 0.</span><span class="sxs-lookup"><span data-stu-id="0cb44-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="0cb44-134">O local em que os retângulos se sobrepõem a cor é magenta porque os valores R e B estão no máximo.</span><span class="sxs-lookup"><span data-stu-id="0cb44-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="0cb44-135">Aqui está outra imagem de exemplo com código.</span><span class="sxs-lookup"><span data-stu-id="0cb44-135">Here's another example image with code.</span></span>



| <span data-ttu-id="0cb44-136">Antes da imagem 1</span><span class="sxs-lookup"><span data-stu-id="0cb44-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg)    |
| <span data-ttu-id="0cb44-138">Antes da imagem 2</span><span class="sxs-lookup"><span data-stu-id="0cb44-138">Before image 2</span></span>                                                             |
| ![a segunda imagem antes do efeito.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="0cb44-140">After (após)</span><span class="sxs-lookup"><span data-stu-id="0cb44-140">After</span></span>                                                                      |
| ![a imagem após a transformação.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="0cb44-142">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="0cb44-142">Effect properties</span></span>



| <span data-ttu-id="0cb44-143">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="0cb44-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="0cb44-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cb44-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb44-145">Coeficientes</span><span class="sxs-lookup"><span data-stu-id="0cb44-145">Coefficients</span></span><br/> <span data-ttu-id="0cb44-146">Coeficientes de prop D2D1 \_ ARITHMETICCOMPOSITE \_ \_</span><span class="sxs-lookup"><span data-stu-id="0cb44-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="0cb44-147">Os coeficientes da equação usados para compor as duas imagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="0cb44-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="0cb44-148">Os coeficientes são sem limite e sem limites.</span><span class="sxs-lookup"><span data-stu-id="0cb44-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="0cb44-149">Type é D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="0cb44-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="0cb44-150">O valor padrão é {1,0 f, 0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="0cb44-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="0cb44-151">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="0cb44-151">ClampOutput</span></span><br/> <span data-ttu-id="0cb44-152">\_Saída d2d1 ARITHMETICCOMPOSITE \_ prop \_ fixe \_</span><span class="sxs-lookup"><span data-stu-id="0cb44-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="0cb44-153">O efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo.</span><span class="sxs-lookup"><span data-stu-id="0cb44-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="0cb44-154">Se você definir isso como verdadeiro, o efeito irá fixe os valores.</span><span class="sxs-lookup"><span data-stu-id="0cb44-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="0cb44-155">Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.</span><span class="sxs-lookup"><span data-stu-id="0cb44-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="0cb44-156">O tipo é BOOL.</span><span class="sxs-lookup"><span data-stu-id="0cb44-156">Type is BOOL.</span></span><br/> <span data-ttu-id="0cb44-157">O valor padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="0cb44-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="0cb44-158">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="0cb44-158">Output bitmap</span></span>

<span data-ttu-id="0cb44-159">O bitmap de saída depende dos valores de coeficiente.</span><span class="sxs-lookup"><span data-stu-id="0cb44-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="0cb44-160">Esses são os tamanhos de bitmap de saída possíveis.</span><span class="sxs-lookup"><span data-stu-id="0cb44-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="0cb44-161">Se C1 for o único coeficiente diferente de zero, o tamanho de saída será a interseção dos retângulos de entrada.</span><span class="sxs-lookup"><span data-stu-id="0cb44-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="0cb44-162">Se C2 for o único coeficiente diferente de zero, o tamanho de saída será o tamanho do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="0cb44-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="0cb44-163">Se C3 for o único coeficiente diferente de zero, o tamanho de saída será o tamanho do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="0cb44-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="0cb44-164">Se todos os coeficientes forem zero, o tamanho de saída será um retângulo vazio.</span><span class="sxs-lookup"><span data-stu-id="0cb44-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="0cb44-165">Para todos os outros valores de coeficiente, o tamanho de saída é a União dos retângulos de entrada.</span><span class="sxs-lookup"><span data-stu-id="0cb44-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb44-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb44-166">Requirements</span></span>



| <span data-ttu-id="0cb44-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb44-167">Requirement</span></span> | <span data-ttu-id="0cb44-168">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb44-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb44-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb44-169">Minimum supported client</span></span> | <span data-ttu-id="0cb44-170">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0cb44-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0cb44-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb44-171">Minimum supported server</span></span> | <span data-ttu-id="0cb44-172">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0cb44-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0cb44-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cb44-173">Header</span></span>                   | <span data-ttu-id="0cb44-174">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="0cb44-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0cb44-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cb44-175">Library</span></span>                  | <span data-ttu-id="0cb44-176">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0cb44-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0cb44-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cb44-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cb44-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0cb44-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

