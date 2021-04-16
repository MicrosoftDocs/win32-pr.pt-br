---
title: Efeito de transformação 3D
description: Use o efeito de transformação 3D para aplicar uma matriz de transformação 4x4 arbitrária a uma imagem.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- efeito de transformação 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570961"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="2ca92-104">Efeito de transformação 3D</span><span class="sxs-lookup"><span data-stu-id="2ca92-104">3D transform effect</span></span>

<span data-ttu-id="2ca92-105">Use o efeito de transformação 3D para aplicar uma matriz de transformação 4x4 arbitrária a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2ca92-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="2ca92-106">Esse efeito aplica a matriz (M?) que você fornece aos vértices de canto da imagem de origem ( \[ x y z 1 \] ) usando este cálculo:</span><span class="sxs-lookup"><span data-stu-id="2ca92-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="2ca92-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?</span><span class="sxs-lookup"><span data-stu-id="2ca92-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="2ca92-108">O CLSID para esse efeito é CLSID \_ D2D13DTransform.</span><span class="sxs-lookup"><span data-stu-id="2ca92-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="2ca92-109">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="2ca92-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="2ca92-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="2ca92-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="2ca92-111">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="2ca92-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="2ca92-112">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="2ca92-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="2ca92-113">Classe de matriz de transformação 4x4</span><span class="sxs-lookup"><span data-stu-id="2ca92-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="2ca92-114">Requirements</span><span class="sxs-lookup"><span data-stu-id="2ca92-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2ca92-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ca92-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="2ca92-116">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="2ca92-116">Example image</span></span>



| <span data-ttu-id="2ca92-117">Antes</span><span class="sxs-lookup"><span data-stu-id="2ca92-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![a imagem antes da transformação.](images/default-before.jpg) |
| <span data-ttu-id="2ca92-119">After (após)</span><span class="sxs-lookup"><span data-stu-id="2ca92-119">After</span></span>                                                         |
| ![a imagem após a transformação.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="2ca92-121">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="2ca92-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ca92-122">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="2ca92-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="2ca92-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ca92-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ca92-124">Interpolação</span><span class="sxs-lookup"><span data-stu-id="2ca92-124">InterpolationMode</span></span><br/> <span data-ttu-id="2ca92-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="2ca92-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="2ca92-126">O modo de interpolação usado pelo efeito na imagem.</span><span class="sxs-lookup"><span data-stu-id="2ca92-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="2ca92-127">Há 5 modos de escala que variam de qualidade e velocidade.</span><span class="sxs-lookup"><span data-stu-id="2ca92-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="2ca92-128">O tipo é D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="2ca92-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="2ca92-129">O valor padrão é D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="2ca92-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ca92-130">Bordermode</span><span class="sxs-lookup"><span data-stu-id="2ca92-130">BorderMode</span></span><br/> <span data-ttu-id="2ca92-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="2ca92-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="2ca92-132">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="2ca92-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="2ca92-133">Consulte <a href="https://www.bing.com/search?q=Border+modes">modos de borda</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2ca92-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="2ca92-134">O tipo é D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="2ca92-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="2ca92-135">O valor padrão é D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="2ca92-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ca92-136">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="2ca92-136">TransformMatrix</span></span><br/> <span data-ttu-id="2ca92-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="2ca92-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="2ca92-138">Uma matriz de transformação 4x4 aplicada ao plano de projeção.</span><span class="sxs-lookup"><span data-stu-id="2ca92-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="2ca92-139">O cálculo de matriz a seguir é usado para mapear pontos de um sistema de coordenadas 3D para o sistema de coordenadas 2D transformado.</span><span class="sxs-lookup"><span data-stu-id="2ca92-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="2ca92-140">Em que:</span><span class="sxs-lookup"><span data-stu-id="2ca92-140">Where:</span></span><dl> <span data-ttu-id="2ca92-141">Coordenadas de plano de projeção X, Y, Z = Input</span><span class="sxs-lookup"><span data-stu-id="2ca92-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="2ca92-142">Elementos da matriz M<sub>x, y</sub> = Transform</span><span class="sxs-lookup"><span data-stu-id="2ca92-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="2ca92-143">Coordenadas de plano de projeção X, Y, Z = output</span><span class="sxs-lookup"><span data-stu-id="2ca92-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="2ca92-144">Os elementos da matriz individual não estão limitados e não são de unidade.</span><span class="sxs-lookup"><span data-stu-id="2ca92-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="2ca92-145">O tipo é D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="2ca92-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="2ca92-146">O valor padrão é Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="2ca92-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="2ca92-147">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="2ca92-147">Interpolation modes</span></span>



| <span data-ttu-id="2ca92-148">Enumeração</span><span class="sxs-lookup"><span data-stu-id="2ca92-148">Enumeration</span></span>                                                   | <span data-ttu-id="2ca92-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ca92-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca92-150">D2D1 \_ 3DTRANSFORM \_ modo de interpolação \_ \_ mais próximo \_</span><span class="sxs-lookup"><span data-stu-id="2ca92-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="2ca92-151">Amostra o ponto único mais próximo e o usa.</span><span class="sxs-lookup"><span data-stu-id="2ca92-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="2ca92-152">Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="2ca92-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="2ca92-153">\_Modo de \_ interpolação d2d1 3DTRANSFORM \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="2ca92-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="2ca92-154">Usa uma amostra de quatro pontos e uma interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="2ca92-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="2ca92-155">Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="2ca92-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="2ca92-156">\_Modo de \_ interpolação d2d1 3DTRANSFORM \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="2ca92-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="2ca92-157">Usa um kernel cúbico de 16 amostras para interpolação.</span><span class="sxs-lookup"><span data-stu-id="2ca92-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="2ca92-158">Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="2ca92-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="2ca92-159">\_Modo de \_ interpolação d2d1 3DTRANSFORM com \_ \_ várias \_ amostras \_ lineares</span><span class="sxs-lookup"><span data-stu-id="2ca92-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="2ca92-160">Usa quatro amostras lineares em um único pixel para suavização de multialias de borda.</span><span class="sxs-lookup"><span data-stu-id="2ca92-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="2ca92-161">Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.</span><span class="sxs-lookup"><span data-stu-id="2ca92-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="2ca92-162">\_Modo de \_ interpolação d2d1 3DTRANSFORM \_ \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="2ca92-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="2ca92-163">Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="2ca92-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="2ca92-164">Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ 3DTRANSFORM \_ modo de interpolação \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="2ca92-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="2ca92-165">O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.</span><span class="sxs-lookup"><span data-stu-id="2ca92-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="2ca92-166">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="2ca92-166">Border modes</span></span>



| <span data-ttu-id="2ca92-167">Nome</span><span class="sxs-lookup"><span data-stu-id="2ca92-167">Name</span></span>                     | <span data-ttu-id="2ca92-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ca92-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca92-169">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="2ca92-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="2ca92-170">O efeito preenche a imagem com pixels pretos transparentes à medida que ele interpola, resultando em uma borda suave.</span><span class="sxs-lookup"><span data-stu-id="2ca92-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="2ca92-171">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="2ca92-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="2ca92-172">O efeito coloca a saída para o tamanho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="2ca92-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="2ca92-173">Classe de matriz de transformação 4x4</span><span class="sxs-lookup"><span data-stu-id="2ca92-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="2ca92-174">O Direct2D fornece uma classe de matriz 4x4 para fornecer funções auxiliares para transformar a imagem em 3 dimensões.</span><span class="sxs-lookup"><span data-stu-id="2ca92-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="2ca92-175">Consulte o tópico [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) para obter mais informações e uma descrição de todos os membros de classe.</span><span class="sxs-lookup"><span data-stu-id="2ca92-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="2ca92-176">Função</span><span class="sxs-lookup"><span data-stu-id="2ca92-176">Function</span></span>                                | <span data-ttu-id="2ca92-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ca92-177">Description</span></span>                                                                                    | <span data-ttu-id="2ca92-178">Matriz</span><span class="sxs-lookup"><span data-stu-id="2ca92-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="2ca92-179">Matrix4x4F:: Scale (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="2ca92-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="2ca92-180">Gera uma matriz de transformação que dimensiona o plano de projeção na direção X, Y e/ou Z.</span><span class="sxs-lookup"><span data-stu-id="2ca92-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![matriz scale3d](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="2ca92-182">SkewX (X)</span><span class="sxs-lookup"><span data-stu-id="2ca92-182">SkewX(X)</span></span>                                | <span data-ttu-id="2ca92-183">Gera uma matriz de transformação que inclina o plano de projeção na direção X.</span><span class="sxs-lookup"><span data-stu-id="2ca92-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![Mostra uma matriz de distorção na direção X.](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="2ca92-185">Distorção (Y)</span><span class="sxs-lookup"><span data-stu-id="2ca92-185">SkewY(Y)</span></span>                                | <span data-ttu-id="2ca92-186">Gera uma matriz de transformação que inclina o plano de projeção na direção Y.</span><span class="sxs-lookup"><span data-stu-id="2ca92-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![matriz de distorção](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="2ca92-188">Tradução (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="2ca92-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="2ca92-189">Gera uma matriz de transformação que traduz o plano de projeção na direção X, Y ou Z.</span><span class="sxs-lookup"><span data-stu-id="2ca92-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![traduzir matriz](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="2ca92-191">RotationX (X)</span><span class="sxs-lookup"><span data-stu-id="2ca92-191">RotationX(X)</span></span>                            | <span data-ttu-id="2ca92-192">Gera uma matriz de transformação que gira o plano de projeção sobre o eixo X.</span><span class="sxs-lookup"><span data-stu-id="2ca92-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![girar matriz x](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="2ca92-194">Rotação (Y)</span><span class="sxs-lookup"><span data-stu-id="2ca92-194">RotationY(Y)</span></span>                            | <span data-ttu-id="2ca92-195">Gera uma matriz de transformação que gira o plano de projeção sobre o eixo Y.</span><span class="sxs-lookup"><span data-stu-id="2ca92-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![girar matriz y](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="2ca92-197">RotationZ (Z)</span><span class="sxs-lookup"><span data-stu-id="2ca92-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="2ca92-198">Gera uma matriz de transformação que gira o plano de projeção sobre o eixo Z.</span><span class="sxs-lookup"><span data-stu-id="2ca92-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![girar matriz z](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="2ca92-200">PerspectiveProjection (D)</span><span class="sxs-lookup"><span data-stu-id="2ca92-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="2ca92-201">Uma transformação de perspectiva com um valor de profundidade de D.</span><span class="sxs-lookup"><span data-stu-id="2ca92-201">A perspective transformation with a depth value of D.</span></span>                                          | ![matriz de perspectiva](images/3d-transform-matrix8.png) |
| <span data-ttu-id="2ca92-203">RotationArbitraryAxis (X, Y, Z, graus)</span><span class="sxs-lookup"><span data-stu-id="2ca92-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="2ca92-204">Gira o plano de projeção sobre o eixo que você especificar.</span><span class="sxs-lookup"><span data-stu-id="2ca92-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="2ca92-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca92-205">Requirements</span></span>



| <span data-ttu-id="2ca92-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca92-206">Requirement</span></span> | <span data-ttu-id="2ca92-207">Valor</span><span class="sxs-lookup"><span data-stu-id="2ca92-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca92-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca92-208">Minimum supported client</span></span> | <span data-ttu-id="2ca92-209">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2ca92-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2ca92-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca92-210">Minimum supported server</span></span> | <span data-ttu-id="2ca92-211">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2ca92-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2ca92-212">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ca92-212">Header</span></span>                   | <span data-ttu-id="2ca92-213">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="2ca92-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="2ca92-214">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ca92-214">Library</span></span>                  | <span data-ttu-id="2ca92-215">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2ca92-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2ca92-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ca92-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca92-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="2ca92-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

