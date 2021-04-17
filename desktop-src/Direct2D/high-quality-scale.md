---
title: Efeito de escala
description: Use esse efeito para dimensionar uma imagem para cima ou para baixo. O efeito tem seis modos de dimensionamento vizinhos mais próximos, lineares, cúbicos, lineares de várias amostras, anisotropic e cúbico de alta qualidade.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- efeito de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369534"
---
# <a name="scale-effect"></a><span data-ttu-id="e69bd-105">Efeito de escala</span><span class="sxs-lookup"><span data-stu-id="e69bd-105">Scale effect</span></span>

<span data-ttu-id="e69bd-106">Use esse efeito para dimensionar uma imagem para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="e69bd-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="e69bd-107">O efeito tem seis modos de dimensionamento: vizinho mais próximo, linear, cúbico, linear de várias amostras, anisotropic e cúbico de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="e69bd-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="e69bd-108">O CLSID para esse efeito é CLSID \_ D2D1Scale.</span><span class="sxs-lookup"><span data-stu-id="e69bd-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="e69bd-109">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="e69bd-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e69bd-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="e69bd-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="e69bd-111">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="e69bd-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="e69bd-112">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="e69bd-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="e69bd-113">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="e69bd-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e69bd-114">Requirements</span><span class="sxs-lookup"><span data-stu-id="e69bd-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e69bd-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e69bd-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e69bd-116">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="e69bd-116">Example image</span></span>

<span data-ttu-id="e69bd-117">Este exemplo mostra o efeito de escala zoom em 2 vezes a entrada e o corte para o tamanho original.</span><span class="sxs-lookup"><span data-stu-id="e69bd-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="e69bd-118">Antes</span><span class="sxs-lookup"><span data-stu-id="e69bd-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| <span data-ttu-id="e69bd-120">After (após)</span><span class="sxs-lookup"><span data-stu-id="e69bd-120">After</span></span>                                                      |
| ![a imagem após a transformação.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="e69bd-122">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="e69bd-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e69bd-123">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="e69bd-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="e69bd-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="e69bd-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e69bd-125">Escala</span><span class="sxs-lookup"><span data-stu-id="e69bd-125">Scale</span></span><br/> <span data-ttu-id="e69bd-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="e69bd-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="e69bd-127">O valor da escala na direção X e Y como uma proporção do tamanho de saída para o tamanho de entrada.</span><span class="sxs-lookup"><span data-stu-id="e69bd-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="e69bd-128">Essa propriedade é D2D1_VECTOR_2Fdefined como: (escala X, escala Y).</span><span class="sxs-lookup"><span data-stu-id="e69bd-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="e69bd-129">Os valores de escala são FLOAT,less, e devem ser positivos ou 0.</span><span class="sxs-lookup"><span data-stu-id="e69bd-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="e69bd-130">O tipo é D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="e69bd-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="e69bd-131">O valor padrão é {1,0 f, 1,0 f}.</span><span class="sxs-lookup"><span data-stu-id="e69bd-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e69bd-132">CenterPoint</span><span class="sxs-lookup"><span data-stu-id="e69bd-132">CenterPoint</span></span><br/> <span data-ttu-id="e69bd-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="e69bd-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="e69bd-134">O ponto do centro de dimensionamento de imagens.</span><span class="sxs-lookup"><span data-stu-id="e69bd-134">The image scaling center point.</span></span> <span data-ttu-id="e69bd-135">Essa propriedade é uma D2D1_VECTOR_2F definida como: (ponto X, ponto Y).</span><span class="sxs-lookup"><span data-stu-id="e69bd-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="e69bd-136">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="e69bd-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="e69bd-137">Use a propriedade do ponto central para dimensionar um ponto que não seja o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="e69bd-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="e69bd-138">O tipo é D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="e69bd-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="e69bd-139">O valor padrão é {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="e69bd-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e69bd-140">Bordermode</span><span class="sxs-lookup"><span data-stu-id="e69bd-140">BorderMode</span></span><br/> <span data-ttu-id="e69bd-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="e69bd-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="e69bd-142">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="e69bd-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="e69bd-143">Consulte <a href="#border-modes">modos de borda</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e69bd-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="e69bd-144">O tipo é D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="e69bd-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="e69bd-145">O valor padrão é D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="e69bd-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e69bd-146">Nitidez</span><span class="sxs-lookup"><span data-stu-id="e69bd-146">Sharpness</span></span><br/> <span data-ttu-id="e69bd-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="e69bd-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="e69bd-148">No modo de interpolação cubica de alta qualidade, o nível de nitidez do filtro de dimensionamento como um float entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="e69bd-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="e69bd-149">Os valores não são de unidade.</span><span class="sxs-lookup"><span data-stu-id="e69bd-149">The values are unitless.</span></span> <span data-ttu-id="e69bd-150">Você pode usar a nitidez para ajustar a qualidade de uma imagem ao dimensionar a imagem para baixo.</span><span class="sxs-lookup"><span data-stu-id="e69bd-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="e69bd-151">O fator de nitidez afeta a forma do kernel.</span><span class="sxs-lookup"><span data-stu-id="e69bd-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="e69bd-152">Quanto maior o fator de nitidez, menor o kernel.</span><span class="sxs-lookup"><span data-stu-id="e69bd-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e69bd-153">Essa propriedade afeta apenas o modo de interpolação cúbica de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="e69bd-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="e69bd-154">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="e69bd-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="e69bd-155">O valor padrão é 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="e69bd-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e69bd-156">Interpolação</span><span class="sxs-lookup"><span data-stu-id="e69bd-156">InterpolationMode</span></span><br/> <span data-ttu-id="e69bd-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="e69bd-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="e69bd-158">O modo de interpolação que o efeito usa para dimensionar a imagem.</span><span class="sxs-lookup"><span data-stu-id="e69bd-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="e69bd-159">Há 6 modos de escala que variam de qualidade e velocidade.</span><span class="sxs-lookup"><span data-stu-id="e69bd-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="e69bd-160">Consulte <a href="#interpolation-modes">modos de interpolação</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e69bd-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="e69bd-161">O tipo é D2D1_SCALE_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="e69bd-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="e69bd-162">O valor padrão é D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="e69bd-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="e69bd-163">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="e69bd-163">Border modes</span></span>



| <span data-ttu-id="e69bd-164">Nome</span><span class="sxs-lookup"><span data-stu-id="e69bd-164">Name</span></span>                     | <span data-ttu-id="e69bd-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="e69bd-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69bd-166">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="e69bd-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="e69bd-167">O efeito preenche a imagem de entrada com pixels pretos transparentes para exemplos fora dos limites de entrada ao aplicar o kernel de convolução.</span><span class="sxs-lookup"><span data-stu-id="e69bd-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="e69bd-168">Isso cria uma borda suave para a imagem e, no processo, expande o bitmap de saída pelo tamanho do kernel.</span><span class="sxs-lookup"><span data-stu-id="e69bd-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="e69bd-169">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="e69bd-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="e69bd-170">O efeito estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada.</span><span class="sxs-lookup"><span data-stu-id="e69bd-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="e69bd-171">O tamanho do bitmap de saída é igual ao tamanho do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="e69bd-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="e69bd-172">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="e69bd-172">Interpolation modes</span></span>



| <span data-ttu-id="e69bd-173">Enumeração</span><span class="sxs-lookup"><span data-stu-id="e69bd-173">Enumeration</span></span>                                             | <span data-ttu-id="e69bd-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="e69bd-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69bd-175">\_Modo de \_ interpolação de escala d2d1 \_ \_ mais próximo do \_ vizinho</span><span class="sxs-lookup"><span data-stu-id="e69bd-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="e69bd-176">Amostra o ponto único mais próximo e o usa.</span><span class="sxs-lookup"><span data-stu-id="e69bd-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="e69bd-177">Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="e69bd-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="e69bd-178">\_Modo de \_ interpolação de escala d2d1 \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="e69bd-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="e69bd-179">Usa uma amostra de quatro pontos e uma interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="e69bd-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="e69bd-180">Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="e69bd-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="e69bd-181">\_Modo de \_ interpolação de escala d2d1 \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="e69bd-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="e69bd-182">Usa um kernel cúbico de 16 amostras para interpolação.</span><span class="sxs-lookup"><span data-stu-id="e69bd-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="e69bd-183">Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="e69bd-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="e69bd-184">\_Modo de \_ interpolação de escala d2d1 \_ \_ várias \_ amostras \_ lineares</span><span class="sxs-lookup"><span data-stu-id="e69bd-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="e69bd-185">Usa quatro amostras lineares em um único pixel para suavização de multialias de borda.</span><span class="sxs-lookup"><span data-stu-id="e69bd-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="e69bd-186">Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.</span><span class="sxs-lookup"><span data-stu-id="e69bd-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="e69bd-187">\_Modo de \_ interpolação de escala d2d1 \_ \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="e69bd-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="e69bd-188">Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="e69bd-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="e69bd-189">\_Modo de interpolação de escala D2D1do \_ cúbico de \_ \_ alta \_ qualidade \_</span><span class="sxs-lookup"><span data-stu-id="e69bd-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="e69bd-190">Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="e69bd-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="e69bd-191">Em seguida, usa o modo de interpolação cúbica para a saída final.</span><span class="sxs-lookup"><span data-stu-id="e69bd-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="e69bd-192">Se você não selecionar um modo, o efeito terá como padrão o \_ modo de interpolação de escala de d2d1 \_ \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="e69bd-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="e69bd-193">O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.</span><span class="sxs-lookup"><span data-stu-id="e69bd-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="e69bd-194">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="e69bd-194">Output bitmap</span></span>

<span data-ttu-id="e69bd-195">O local e o tamanho do bitmap de saída dependem do fator de escala especificado e do ponto central.</span><span class="sxs-lookup"><span data-stu-id="e69bd-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="e69bd-196">Você pode calcular o tamanho do bitmap de saída usando esta equação:</span><span class="sxs-lookup"><span data-stu-id="e69bd-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="e69bd-197">BitmapSize? (Pixels) = escala? \* Tamanho do bitmap original?</span><span class="sxs-lookup"><span data-stu-id="e69bd-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="e69bd-198">(DIPs) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="e69bd-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="e69bd-199">BitmapSize<sub>y</sub>(pixels) = dimensionar<sub></sub> \* tamanho do bitmap original<sub></sub> y (DIPs) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="e69bd-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="e69bd-200">O efeito arredonda frações de pixels para o pixel inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="e69bd-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="e69bd-201">O local do bitmap é (0, 0) ou o valor da Propriedade do ponto central.</span><span class="sxs-lookup"><span data-stu-id="e69bd-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e69bd-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e69bd-202">Requirements</span></span>



| <span data-ttu-id="e69bd-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="e69bd-203">Requirement</span></span> | <span data-ttu-id="e69bd-204">Valor</span><span class="sxs-lookup"><span data-stu-id="e69bd-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e69bd-205">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e69bd-205">Minimum supported client</span></span> | <span data-ttu-id="e69bd-206">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e69bd-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e69bd-207">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e69bd-207">Minimum supported server</span></span> | <span data-ttu-id="e69bd-208">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e69bd-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e69bd-209">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e69bd-209">Header</span></span>                   | <span data-ttu-id="e69bd-210">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e69bd-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e69bd-211">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e69bd-211">Library</span></span>                  | <span data-ttu-id="e69bd-212">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e69bd-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e69bd-213">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e69bd-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e69bd-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e69bd-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

