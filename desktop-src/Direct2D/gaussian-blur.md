---
title: Efeito de desfoque gaussiano
description: Use o efeito de desfoque gaussiano para criar um desfoque com base na função gaussiana em toda a imagem de entrada.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Desfoque Gaussiano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562327"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="c5e3d-104">Efeito de desfoque gaussiano</span><span class="sxs-lookup"><span data-stu-id="c5e3d-104">Gaussian blur effect</span></span>

<span data-ttu-id="c5e3d-105">Use o efeito de desfoque gaussiano para criar um desfoque com base na função gaussiana em toda a imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="c5e3d-106">Você pode usar esse efeito para criar brilhos e soltar sombras e usar o efeito [composto](composite.md) para aplicar o resultado à imagem original.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="c5e3d-107">Ele é útil no processamento de fotos para filtros como realces e sombras.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="c5e3d-108">Você pode usar a saída desse efeito para entrada em efeitos de iluminação, como os efeitos de iluminação [especular](specular-lighting.md) ou de [iluminação difusa](diffuse-lighting.md) , porque o canal alfa está indefinido e efeitos de iluminação usam o canal alfa para determinar a geometria da superfície como um mapa de altura.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="c5e3d-109">Esse efeito é usado pelo efeito de [sombra](drop-shadow.md) interna.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="c5e3d-110">O CLSID para esse efeito é CLSID \_ D2D1GaussianBlur.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="c5e3d-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="c5e3d-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c5e3d-112">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="c5e3d-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c5e3d-113">Modos de otimização</span><span class="sxs-lookup"><span data-stu-id="c5e3d-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="c5e3d-114">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="c5e3d-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="c5e3d-115">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="c5e3d-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="c5e3d-116">Requirements</span><span class="sxs-lookup"><span data-stu-id="c5e3d-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c5e3d-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5e3d-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c5e3d-118">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="c5e3d-118">Example image</span></span>



| <span data-ttu-id="c5e3d-119">Antes</span><span class="sxs-lookup"><span data-stu-id="c5e3d-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| <span data-ttu-id="c5e3d-121">After (após)</span><span class="sxs-lookup"><span data-stu-id="c5e3d-121">After</span></span>                                                        |
| ![a imagem após a transformação.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="c5e3d-123">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="c5e3d-123">Effect properties</span></span>



| <span data-ttu-id="c5e3d-124">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="c5e3d-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="c5e3d-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5e3d-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e3d-126">I</span><span class="sxs-lookup"><span data-stu-id="c5e3d-126">StandardDeviation</span></span><br/> <span data-ttu-id="c5e3d-127">\_ \_ Desvio padrão da prop d2d1 GAUSSIANBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5e3d-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="c5e3d-128">A quantidade de desfoque a ser aplicada à imagem.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="c5e3d-129">Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="c5e3d-130">As unidades do desvio padrão e do raio de desfoque são DIPs.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="c5e3d-131">Um valor de DIPs zero desabilita totalmente esse efeito.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="c5e3d-132">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="c5e3d-133">O valor padrão é 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="c5e3d-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="c5e3d-134">Optimization</span></span><br/> <span data-ttu-id="c5e3d-135">\_Otimização de \_ prop d2d1 GAUSSIANBLUR \_</span><span class="sxs-lookup"><span data-stu-id="c5e3d-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="c5e3d-136">O modo de otimização.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-136">The optimization mode.</span></span> <span data-ttu-id="c5e3d-137">Consulte [modos de otimização](#optimization-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="c5e3d-138">O tipo é D2D1 \_ GAUSSIANBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="c5e3d-139">O valor padrão é D2D1 \_ GAUSSIANBLUR \_ Optimization \_ baequilibrada.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="c5e3d-140">Bordermode</span><span class="sxs-lookup"><span data-stu-id="c5e3d-140">BorderMode</span></span><br/> <span data-ttu-id="c5e3d-141">\_Modo de \_ borda de prop d2d1 GAUSSIANBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5e3d-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="c5e3d-142">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="c5e3d-143">Consulte [modos de borda](#border-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="c5e3d-144">O tipo é o \_ modo de borda d2d1 GAUSSIANBLUR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c5e3d-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="c5e3d-145">O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c5e3d-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="c5e3d-146">Modos de otimização</span><span class="sxs-lookup"><span data-stu-id="c5e3d-146">Optimization modes</span></span>



| <span data-ttu-id="c5e3d-147">Nome</span><span class="sxs-lookup"><span data-stu-id="c5e3d-147">Name</span></span>                                          | <span data-ttu-id="c5e3d-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5e3d-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e3d-149">Velocidade de otimização do D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5e3d-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="c5e3d-150">Aplica otimizações internas, como o dimensionamento prévio em raios relativamente pequenos.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="c5e3d-151">Usa filtragem linear.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="c5e3d-152">D2D1 \_ DIRECTIONALBLUR de \_ otimização \_ balanceada</span><span class="sxs-lookup"><span data-stu-id="c5e3d-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="c5e3d-153">Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem triline.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="c5e3d-154">\_Qualidade de \_ otimização de DIRECTIONALBLUR d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="c5e3d-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="c5e3d-155">Usa apenas otimizações internas com raios grandes de desfoque, em que as aproximações são menos prováveis de serem visíveis.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="c5e3d-156">Usa a filtragem triline.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="c5e3d-157">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="c5e3d-157">Border modes</span></span>



| <span data-ttu-id="c5e3d-158">Nome</span><span class="sxs-lookup"><span data-stu-id="c5e3d-158">Name</span></span>                     | <span data-ttu-id="c5e3d-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5e3d-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e3d-160">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="c5e3d-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="c5e3d-161">O efeito preenche a imagem com pixels pretos transparentes à medida que aplica o kernel de desfoque, resultando em uma borda suave.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="c5e3d-162">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="c5e3d-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="c5e3d-163">O efeito coloca a saída para o tamanho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="c5e3d-164">Quando o efeito aplica o kernel de desfoque, ele estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="c5e3d-165">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="c5e3d-165">Output bitmap</span></span>

<span data-ttu-id="c5e3d-166">A saída desse efeito pode ser maior do que o bitmap de entrada com base no raio de desfoque e no modo de borda.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="c5e3d-167">Se o modo de borda for definido como \_ d2d1 \_ modo de borda \_ suave, os s imensionar do bitmap de saída aumentará pelo tamanho do kernel de desfoque, representado em pixels.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="c5e3d-168">Esta tabela fornece uma equação que você pode usar para calcular o bitmap de saída.</span><span class="sxs-lookup"><span data-stu-id="c5e3d-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="c5e3d-169">Portanto, se o tamanho da imagem aumentar por 10 pixels em cada direção, o canto superior esquerdo da imagem estará localizado em (-5,-5), enquanto o direito inferior estará em (105, 105).</span><span class="sxs-lookup"><span data-stu-id="c5e3d-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e3d-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e3d-170">Requirements</span></span>



| <span data-ttu-id="c5e3d-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e3d-171">Requirement</span></span> | <span data-ttu-id="c5e3d-172">Valor</span><span class="sxs-lookup"><span data-stu-id="c5e3d-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e3d-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5e3d-173">Minimum supported client</span></span> | <span data-ttu-id="c5e3d-174">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c5e3d-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c5e3d-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5e3d-175">Minimum supported server</span></span> | <span data-ttu-id="c5e3d-176">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c5e3d-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c5e3d-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5e3d-177">Header</span></span>                   | <span data-ttu-id="c5e3d-178">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c5e3d-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c5e3d-179">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5e3d-179">Library</span></span>                  | <span data-ttu-id="c5e3d-180">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c5e3d-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c5e3d-181">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5e3d-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5e3d-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c5e3d-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

