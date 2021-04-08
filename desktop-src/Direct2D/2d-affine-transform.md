---
title: Efeito de transformação afim 2D
description: O efeito de transformação afim 2D aplica uma transformação espacial a uma imagem com base em uma matriz 3X2 usando a transformação matriz Direct2D e qualquer um dos seis modos de interpolação.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Efeito de transformação afim 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086517"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="18709-104">Efeito de transformação afim 2D</span><span class="sxs-lookup"><span data-stu-id="18709-104">2D affine transform effect</span></span>

<span data-ttu-id="18709-105">O efeito de transformação afim 2D aplica uma transformação espacial a uma imagem com base em uma matriz 3X2 usando a [transformação](direct2d-transforms-overview.md) matriz Direct2D e qualquer um dos seis modos de interpolação.</span><span class="sxs-lookup"><span data-stu-id="18709-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="18709-106">Você pode usar esse efeito para girar, dimensionar, inclinar ou traduzir uma imagem.</span><span class="sxs-lookup"><span data-stu-id="18709-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="18709-107">Ou você pode combinar essas operações.</span><span class="sxs-lookup"><span data-stu-id="18709-107">Or, you can combine these operations.</span></span> <span data-ttu-id="18709-108">As transferências afim preservam as linhas paralelas e a proporção de distâncias entre os três pontos de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="18709-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="18709-109">O CLSID para esse efeito é CLSID \_ D2D12DAffineTransform.</span><span class="sxs-lookup"><span data-stu-id="18709-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="18709-110">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="18709-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="18709-111">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="18709-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="18709-112">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="18709-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="18709-113">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="18709-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="18709-114">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="18709-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="18709-115">Requirements</span><span class="sxs-lookup"><span data-stu-id="18709-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="18709-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18709-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="18709-117">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="18709-117">Example image</span></span>



| <span data-ttu-id="18709-118">Antes</span><span class="sxs-lookup"><span data-stu-id="18709-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)         |
| <span data-ttu-id="18709-120">After (após)</span><span class="sxs-lookup"><span data-stu-id="18709-120">After</span></span>                                                              |
| ![a imagem após a transformação.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="18709-122">Esse efeito executa essa operação de matriz:</span><span class="sxs-lookup"><span data-stu-id="18709-122">This effect performs this matrix operation:</span></span>

![operação de matriz afim](images/affine-matrix-calculation.png)

<span data-ttu-id="18709-124">Embora a matriz de entrada seja definida como uma matriz 3x2, a última coluna é preenchida com 0, 0 e 1 para produzir uma matriz quadrada.</span><span class="sxs-lookup"><span data-stu-id="18709-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="18709-125">Isso permite a multiplicação de matriz, para que as transformações possam ser concatenadas em uma única matriz.</span><span class="sxs-lookup"><span data-stu-id="18709-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="18709-126">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="18709-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18709-127">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="18709-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="18709-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="18709-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18709-129">Interpolação</span><span class="sxs-lookup"><span data-stu-id="18709-129">InterpolationMode</span></span><br/> <span data-ttu-id="18709-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="18709-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="18709-131">O modo de interpolação usado para dimensionar a imagem.</span><span class="sxs-lookup"><span data-stu-id="18709-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="18709-132">Há 6 modos de escala que variam de qualidade e velocidade.</span><span class="sxs-lookup"><span data-stu-id="18709-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="18709-133">O tipo é D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="18709-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="18709-134">O valor padrão é D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="18709-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18709-135">Bordermode</span><span class="sxs-lookup"><span data-stu-id="18709-135">BorderMode</span></span><br/> <span data-ttu-id="18709-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="18709-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="18709-137">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="18709-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="18709-138">Consulte <a href="https://www.bing.com/search?q=Border+modes">modos de borda</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="18709-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="18709-139">O tipo é D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="18709-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="18709-140">O valor padrão é D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="18709-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18709-141">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="18709-141">TransformMatrix</span></span><br/> <span data-ttu-id="18709-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="18709-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="18709-143">A matriz 3x2 para transformar a imagem usando a <a href="direct2d-transforms-overview.md">transformação</a>de matriz Direct2D.</span><span class="sxs-lookup"><span data-stu-id="18709-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="18709-144">O tipo é D2D1_MATRIX_3X2_F.</span><span class="sxs-lookup"><span data-stu-id="18709-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="18709-145">O valor padrão é Matrix3x2F:: Identity ().</span><span class="sxs-lookup"><span data-stu-id="18709-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18709-146">Nitidez</span><span class="sxs-lookup"><span data-stu-id="18709-146">Sharpness</span></span><br/> <span data-ttu-id="18709-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="18709-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="18709-148">No modo de interpolação cubica de alta qualidade, o nível de nitidez do filtro de dimensionamento como um float entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="18709-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="18709-149">Os valores não são de unidade.</span><span class="sxs-lookup"><span data-stu-id="18709-149">The values are unitless.</span></span> <span data-ttu-id="18709-150">Você pode usar a nitidez para ajustar a qualidade de uma imagem ao dimensionar a imagem.</span><span class="sxs-lookup"><span data-stu-id="18709-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="18709-151">O fator de nitidez afeta a forma do kernel.</span><span class="sxs-lookup"><span data-stu-id="18709-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="18709-152">Quanto maior o fator de nitidez, menor o kernel.</span><span class="sxs-lookup"><span data-stu-id="18709-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="18709-153">Essa propriedade afeta apenas o modo de interpolação cúbica de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="18709-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="18709-154">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="18709-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="18709-155">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="18709-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="18709-156">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="18709-156">Border modes</span></span>



| <span data-ttu-id="18709-157">Nome</span><span class="sxs-lookup"><span data-stu-id="18709-157">Name</span></span>                     | <span data-ttu-id="18709-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="18709-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18709-159">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="18709-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="18709-160">O efeito preenche a imagem com pixels pretos transparentes à medida que ele interpola, resultando em uma borda suave.</span><span class="sxs-lookup"><span data-stu-id="18709-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="18709-161">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="18709-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="18709-162">O efeito coloca a saída para o tamanho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="18709-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="18709-163">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="18709-163">Interpolation modes</span></span>



| <span data-ttu-id="18709-164">Enumeração</span><span class="sxs-lookup"><span data-stu-id="18709-164">Enumeration</span></span>                                                         | <span data-ttu-id="18709-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="18709-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18709-166">D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolação \_ \_ mais próximo \_</span><span class="sxs-lookup"><span data-stu-id="18709-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="18709-167">Amostra o ponto único mais próximo e o usa.</span><span class="sxs-lookup"><span data-stu-id="18709-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="18709-168">Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="18709-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="18709-169">\_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="18709-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="18709-170">Usa uma amostra de quatro pontos e uma interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="18709-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="18709-171">Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="18709-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="18709-172">\_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="18709-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="18709-173">Usa um kernel cúbico de 16 amostras para interpolação.</span><span class="sxs-lookup"><span data-stu-id="18709-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="18709-174">Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="18709-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="18709-175">\_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM com \_ \_ várias \_ amostras \_ lineares</span><span class="sxs-lookup"><span data-stu-id="18709-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="18709-176">Usa quatro amostras lineares em um único pixel para suavização de multialias de borda.</span><span class="sxs-lookup"><span data-stu-id="18709-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="18709-177">Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.</span><span class="sxs-lookup"><span data-stu-id="18709-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="18709-178">\_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM \_ \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="18709-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="18709-179">Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="18709-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="18709-180">\_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM de \_ \_ alta \_ qualidade \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="18709-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="18709-181">Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="18709-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="18709-182">Em seguida, usa o modo de interpolação cúbica para a saída final.</span><span class="sxs-lookup"><span data-stu-id="18709-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="18709-183">Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolação \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="18709-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="18709-184">O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.</span><span class="sxs-lookup"><span data-stu-id="18709-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="18709-185">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="18709-185">Output bitmap</span></span>

<span data-ttu-id="18709-186">O tamanho do bitmap de saída depende da matriz de transformação aplicada à imagem.</span><span class="sxs-lookup"><span data-stu-id="18709-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="18709-187">O efeito executa a operação de transformação e, em seguida, aplica uma caixa delimitadora em volta do resultado.</span><span class="sxs-lookup"><span data-stu-id="18709-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="18709-188">O bitmap de saída é o tamanho da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="18709-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="18709-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18709-189">Requirements</span></span>



| <span data-ttu-id="18709-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="18709-190">Requirement</span></span> | <span data-ttu-id="18709-191">Valor</span><span class="sxs-lookup"><span data-stu-id="18709-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18709-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18709-192">Minimum supported client</span></span> | <span data-ttu-id="18709-193">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="18709-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="18709-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18709-194">Minimum supported server</span></span> | <span data-ttu-id="18709-195">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="18709-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="18709-196">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18709-196">Header</span></span>                   | <span data-ttu-id="18709-197">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="18709-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="18709-198">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18709-198">Library</span></span>                  | <span data-ttu-id="18709-199">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="18709-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="18709-200">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18709-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18709-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="18709-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

