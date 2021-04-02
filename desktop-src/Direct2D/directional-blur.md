---
title: Efeito de desfoque direcional
description: O efeito de desfoque direcional é semelhante ao Desfoque Gaussiano, exceto que você pode distorcer o desfoque em uma direção específica.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- desfoque direcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644238"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="6513e-104">Efeito de desfoque direcional</span><span class="sxs-lookup"><span data-stu-id="6513e-104">Directional blur effect</span></span>

<span data-ttu-id="6513e-105">O efeito de desfoque direcional é semelhante ao [Desfoque Gaussiano](gaussian-blur.md), exceto que você pode distorcer o desfoque em uma direção específica.</span><span class="sxs-lookup"><span data-stu-id="6513e-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="6513e-106">Você pode usar esse efeito para fazer com que uma imagem pareça se ela está em movimento ou para enfatizar uma imagem animada.</span><span class="sxs-lookup"><span data-stu-id="6513e-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="6513e-107">O CLSID para esse efeito é CLSID \_ D2D1DirectionalBlur.</span><span class="sxs-lookup"><span data-stu-id="6513e-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="6513e-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="6513e-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="6513e-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="6513e-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6513e-110">Modos de otimização</span><span class="sxs-lookup"><span data-stu-id="6513e-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="6513e-111">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="6513e-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="6513e-112">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="6513e-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="6513e-113">Requirements</span><span class="sxs-lookup"><span data-stu-id="6513e-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6513e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6513e-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6513e-115">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="6513e-115">Example image</span></span>



| <span data-ttu-id="6513e-116">Antes</span><span class="sxs-lookup"><span data-stu-id="6513e-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)      |
| <span data-ttu-id="6513e-118">After (após)</span><span class="sxs-lookup"><span data-stu-id="6513e-118">After</span></span>                                                           |
| ![a imagem após a transformação.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="6513e-120">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="6513e-120">Effect properties</span></span>



| <span data-ttu-id="6513e-121">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="6513e-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="6513e-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6513e-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6513e-123">I</span><span class="sxs-lookup"><span data-stu-id="6513e-123">StandardDeviation</span></span><br/> <span data-ttu-id="6513e-124">\_ \_ Desvio padrão da prop d2d1 DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6513e-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="6513e-125">A quantidade de desfoque a ser aplicada à imagem.</span><span class="sxs-lookup"><span data-stu-id="6513e-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="6513e-126">Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3.</span><span class="sxs-lookup"><span data-stu-id="6513e-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="6513e-127">As unidades do desvio padrão e do raio de desfoque são DIPs.</span><span class="sxs-lookup"><span data-stu-id="6513e-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="6513e-128">Um valor de 0 DIPs desabilita esse efeito.</span><span class="sxs-lookup"><span data-stu-id="6513e-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="6513e-129">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="6513e-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="6513e-130">O valor padrão é 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="6513e-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="6513e-131">Ângulo</span><span class="sxs-lookup"><span data-stu-id="6513e-131">Angle</span></span><br/> <span data-ttu-id="6513e-132">\_Ângulo de \_ prop d2d1 DIRECTIONALBLUR \_</span><span class="sxs-lookup"><span data-stu-id="6513e-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="6513e-133">O ângulo do Desfoque relativo ao eixo x, na direção no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="6513e-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="6513e-134">As unidades são especificadas em graus.</span><span class="sxs-lookup"><span data-stu-id="6513e-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="6513e-135">O kernel de desfoque é gerado pela primeira vez usando o mesmo processo para o efeito de [Desfoque Gaussiano](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="6513e-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="6513e-136">Os valores de kernel são então transformados de acordo com o ângulo de desfoque.</span><span class="sxs-lookup"><span data-stu-id="6513e-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="6513e-137">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="6513e-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="6513e-138">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="6513e-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="6513e-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="6513e-139">Optimization</span></span><br/> <span data-ttu-id="6513e-140">\_Otimização de \_ prop d2d1 DIRECTIONALBLUR \_</span><span class="sxs-lookup"><span data-stu-id="6513e-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="6513e-141">O modo de otimização.</span><span class="sxs-lookup"><span data-stu-id="6513e-141">The optimization mode.</span></span> <span data-ttu-id="6513e-142">Consulte [modos de otimização](#optimization-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6513e-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="6513e-143">O tipo é D2D1 \_ DIRECTIONALBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="6513e-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="6513e-144">O valor padrão é D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ baequilibrada.</span><span class="sxs-lookup"><span data-stu-id="6513e-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="6513e-145">Bordermode</span><span class="sxs-lookup"><span data-stu-id="6513e-145">BorderMode</span></span><br/> <span data-ttu-id="6513e-146">\_Modo de \_ borda de prop d2d1 DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6513e-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="6513e-147">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="6513e-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="6513e-148">Consulte [modos de borda](#border-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6513e-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="6513e-149">O tipo é o \_ modo de borda d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="6513e-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="6513e-150">O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6513e-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="6513e-151">Modos de otimização</span><span class="sxs-lookup"><span data-stu-id="6513e-151">Optimization modes</span></span>



| <span data-ttu-id="6513e-152">Nome</span><span class="sxs-lookup"><span data-stu-id="6513e-152">Name</span></span>                                          | <span data-ttu-id="6513e-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="6513e-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6513e-154">Velocidade de otimização do D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6513e-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="6513e-155">Aplica otimizações internas, como o dimensionamento prévio em raios relativamente pequenos.</span><span class="sxs-lookup"><span data-stu-id="6513e-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="6513e-156">Usa filtragem linear.</span><span class="sxs-lookup"><span data-stu-id="6513e-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="6513e-157">D2D1 \_ DIRECTIONALBLUR de \_ otimização \_ balanceada</span><span class="sxs-lookup"><span data-stu-id="6513e-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="6513e-158">Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem triline.</span><span class="sxs-lookup"><span data-stu-id="6513e-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="6513e-159">\_Qualidade de \_ otimização de DIRECTIONALBLUR d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="6513e-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="6513e-160">Usa apenas otimizações internas com raios grandes de desfoque, em que as aproximações são menos prováveis de serem visíveis.</span><span class="sxs-lookup"><span data-stu-id="6513e-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="6513e-161">Usa a filtragem triline.</span><span class="sxs-lookup"><span data-stu-id="6513e-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="6513e-162">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="6513e-162">Border modes</span></span>



| <span data-ttu-id="6513e-163">Nome</span><span class="sxs-lookup"><span data-stu-id="6513e-163">Name</span></span>                     | <span data-ttu-id="6513e-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="6513e-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6513e-165">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="6513e-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="6513e-166">O efeito preenche a imagem com pixels pretos transparentes à medida que aplica o kernel de desfoque, resultando em uma borda suave.</span><span class="sxs-lookup"><span data-stu-id="6513e-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="6513e-167">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="6513e-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="6513e-168">O efeito coloca a saída para o tamanho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="6513e-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="6513e-169">Quando o efeito aplica o kernel de desfoque, ele estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada.</span><span class="sxs-lookup"><span data-stu-id="6513e-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="6513e-170">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="6513e-170">Output bitmap</span></span>

<span data-ttu-id="6513e-171">O tamanho do bitmap de saída aumenta com base no desvio padrão, no ângulo do efeito e no modo de borda.</span><span class="sxs-lookup"><span data-stu-id="6513e-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="6513e-172">Se o modo de borda for definido como \_ d2d1 \_ modo \_ de borda suave, o tamanho do bitmap de saída aumentará pelo tamanho do kernel de desfoque, representado em pixels.</span><span class="sxs-lookup"><span data-stu-id="6513e-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="6513e-173">Essas equações podem ser usadas para calcular o tamanho do bitmap de saída.</span><span class="sxs-lookup"><span data-stu-id="6513e-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="6513e-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="6513e-174">Requirement</span></span> | <span data-ttu-id="6513e-175">Valor</span><span class="sxs-lookup"><span data-stu-id="6513e-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6513e-176">Crescimento de bitmap de saída X</span><span class="sxs-lookup"><span data-stu-id="6513e-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="6513e-177">I (DIPs) \* 6 \* ((DPI do usuário)/96) \* cos (ângulo))</span><span class="sxs-lookup"><span data-stu-id="6513e-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="6513e-178">Crescimento de bitmap de saída Y</span><span class="sxs-lookup"><span data-stu-id="6513e-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="6513e-179">I (DIPs) \* 6 \* ((DPI do usuário)/96) \* sin (ângulo))</span><span class="sxs-lookup"><span data-stu-id="6513e-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6513e-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6513e-180">Requirements</span></span>



| <span data-ttu-id="6513e-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="6513e-181">Requirement</span></span> | <span data-ttu-id="6513e-182">Valor</span><span class="sxs-lookup"><span data-stu-id="6513e-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6513e-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6513e-183">Minimum supported client</span></span> | <span data-ttu-id="6513e-184">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="6513e-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6513e-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6513e-185">Minimum supported server</span></span> | <span data-ttu-id="6513e-186">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="6513e-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6513e-187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6513e-187">Header</span></span>                   | <span data-ttu-id="6513e-188">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6513e-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6513e-189">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6513e-189">Library</span></span>                  | <span data-ttu-id="6513e-190">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6513e-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6513e-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6513e-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6513e-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6513e-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

