---
title: Efeito de sombra
description: Use o efeito de sombra para gerar uma sombra do canal alfa de uma imagem.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- efeito de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294766"
---
# <a name="shadow-effect"></a><span data-ttu-id="e5db0-104">Efeito de sombra</span><span class="sxs-lookup"><span data-stu-id="e5db0-104">Shadow effect</span></span>

<span data-ttu-id="e5db0-105">Use o efeito de sombra para gerar uma sombra do canal alfa de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="e5db0-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="e5db0-106">A sombra é mais opaca para valores Alfa mais altos e mais transparente para valores Alfa inferiores.</span><span class="sxs-lookup"><span data-stu-id="e5db0-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="e5db0-107">Você pode definir a quantidade de desfoque e a cor da sombra.</span><span class="sxs-lookup"><span data-stu-id="e5db0-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="e5db0-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="e5db0-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e5db0-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="e5db0-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e5db0-110">Modos de otimização</span><span class="sxs-lookup"><span data-stu-id="e5db0-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="e5db0-111">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="e5db0-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e5db0-112">Requirements</span><span class="sxs-lookup"><span data-stu-id="e5db0-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e5db0-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5db0-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="e5db0-114">O CLSID para esse efeito é CLSID \_ D2D1Shadow.</span><span class="sxs-lookup"><span data-stu-id="e5db0-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="e5db0-115">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="e5db0-115">Example image</span></span>

<span data-ttu-id="e5db0-116">O exemplo aqui mostra a saída do efeito de sombra traduzida para baixo e para a direita com a imagem de origem composta por ela no local original.</span><span class="sxs-lookup"><span data-stu-id="e5db0-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="e5db0-117">O efeito de sombra só gera a sombra.</span><span class="sxs-lookup"><span data-stu-id="e5db0-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="e5db0-118">Antes</span><span class="sxs-lookup"><span data-stu-id="e5db0-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![a imagem antes do efeito.](images/8-crop.png)      |
| <span data-ttu-id="e5db0-120">After (após)</span><span class="sxs-lookup"><span data-stu-id="e5db0-120">After</span></span>                                                   |
| ![a imagem após a transformação.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="e5db0-122">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="e5db0-122">Effect properties</span></span>



| <span data-ttu-id="e5db0-123">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="e5db0-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="e5db0-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5db0-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5db0-125">BlurStandardDeviation</span><span class="sxs-lookup"><span data-stu-id="e5db0-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="e5db0-126">\_ \_ \_ Desvio padrão de desfoque da d2d1 Shadow prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5db0-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="e5db0-127">A quantidade de desfoque a ser aplicada ao canal alfa da imagem.</span><span class="sxs-lookup"><span data-stu-id="e5db0-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="e5db0-128">Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3.</span><span class="sxs-lookup"><span data-stu-id="e5db0-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="e5db0-129">As unidades do desvio padrão e do raio de desfoque são DIPs.</span><span class="sxs-lookup"><span data-stu-id="e5db0-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="e5db0-130">Essa propriedade é igual à propriedade de desvio padrão de [Desfoque Gaussiano](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="e5db0-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="e5db0-131">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="e5db0-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="e5db0-132">O valor padrão é 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="e5db0-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="e5db0-133">Cor</span><span class="sxs-lookup"><span data-stu-id="e5db0-133">Color</span></span><br/> <span data-ttu-id="e5db0-134">\_Cor de \_ prop d2d1 Shadow \_</span><span class="sxs-lookup"><span data-stu-id="e5db0-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="e5db0-135">A cor da sombra.</span><span class="sxs-lookup"><span data-stu-id="e5db0-135">The color of the drop shadow.</span></span> <span data-ttu-id="e5db0-136">Essa propriedade é um \_ vetor d2d1 \_ 4F definido como: (R, G, B, a).</span><span class="sxs-lookup"><span data-stu-id="e5db0-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="e5db0-137">Você deve especificar essa cor em alfa linear.</span><span class="sxs-lookup"><span data-stu-id="e5db0-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="e5db0-138">O tipo é \_ 4F de vetor d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="e5db0-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="e5db0-139">O valor padrão é {0,0 f, 0,0 f, 0,0 f, 1,0 f}.</span><span class="sxs-lookup"><span data-stu-id="e5db0-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="e5db0-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="e5db0-140">Optimization</span></span><br/> <span data-ttu-id="e5db0-141">\_Otimização da \_ prop d2d1 Shadow \_</span><span class="sxs-lookup"><span data-stu-id="e5db0-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="e5db0-142">O nível de otimização de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e5db0-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="e5db0-143">O tipo é \_ otimização de sombra d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="e5db0-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="e5db0-144">O valor padrão é D2D1 \_ de \_ otimização de sombra \_ .</span><span class="sxs-lookup"><span data-stu-id="e5db0-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="e5db0-145">Modos de otimização</span><span class="sxs-lookup"><span data-stu-id="e5db0-145">Optimization modes</span></span>



| <span data-ttu-id="e5db0-146">Nome</span><span class="sxs-lookup"><span data-stu-id="e5db0-146">Name</span></span>                                          | <span data-ttu-id="e5db0-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5db0-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5db0-148">Velocidade de otimização do D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5db0-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="e5db0-149">Aplica otimizações internas, como o dimensionamento prévio em raios relativamente pequenos.</span><span class="sxs-lookup"><span data-stu-id="e5db0-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="e5db0-150">Usa filtragem linear.</span><span class="sxs-lookup"><span data-stu-id="e5db0-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="e5db0-151">D2D1 \_ DIRECTIONALBLUR de \_ otimização \_ balanceada</span><span class="sxs-lookup"><span data-stu-id="e5db0-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="e5db0-152">Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem triline.</span><span class="sxs-lookup"><span data-stu-id="e5db0-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="e5db0-153">\_Qualidade de \_ otimização de DIRECTIONALBLUR d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="e5db0-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="e5db0-154">Usa apenas otimizações internas com raios grandes de desfoque, em que as aproximações são menos prováveis de serem visíveis.</span><span class="sxs-lookup"><span data-stu-id="e5db0-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="e5db0-155">Usa a filtragem triline.</span><span class="sxs-lookup"><span data-stu-id="e5db0-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="e5db0-156">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="e5db0-156">Output bitmap</span></span>

<span data-ttu-id="e5db0-157">O tamanho do bitmap de saída é o tamanho da saída de desfoque.</span><span class="sxs-lookup"><span data-stu-id="e5db0-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="e5db0-158">A quantidade de crescimento do bitmap de saída em relação ao bitmap original pode ser calculada usando a seguinte equação:</span><span class="sxs-lookup"><span data-stu-id="e5db0-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="e5db0-159">Crescimento do bitmap de saída (X e Y) = BlurStandardDeviation (pixels independentes do dispositivo (DIPs)) \* 6 \* (DPI do usuário)/96</span><span class="sxs-lookup"><span data-stu-id="e5db0-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="e5db0-160">A saída aumenta igualmente em todas as direções, por exemplo, se o tamanho aumenta por 10 pixels em cada direção, o canto superior esquerdo do bitmap está localizado em (-5,-5) e o direito inferior estará em (105, 105), conforme mostrado no diagrama aqui.</span><span class="sxs-lookup"><span data-stu-id="e5db0-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![diagrama de crescimento do tamanho de saída do efeito de sombra.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="e5db0-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5db0-162">Requirements</span></span>



| <span data-ttu-id="e5db0-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5db0-163">Requirement</span></span> | <span data-ttu-id="e5db0-164">Valor</span><span class="sxs-lookup"><span data-stu-id="e5db0-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5db0-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5db0-165">Minimum supported client</span></span> | <span data-ttu-id="e5db0-166">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e5db0-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e5db0-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5db0-167">Minimum supported server</span></span> | <span data-ttu-id="e5db0-168">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e5db0-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e5db0-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5db0-169">Header</span></span>                   | <span data-ttu-id="e5db0-170">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e5db0-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e5db0-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5db0-171">Library</span></span>                  | <span data-ttu-id="e5db0-172">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e5db0-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e5db0-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5db0-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5db0-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e5db0-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

