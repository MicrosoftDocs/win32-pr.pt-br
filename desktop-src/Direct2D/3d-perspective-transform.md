---
title: Efeito de transformação de perspectiva 3D
description: Use o efeito de transformação de perspectiva 3D para girar a imagem em 3 dimensões como se fosse exibida de uma distância.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- efeito de transformação de perspectiva 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824835"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="9c42f-104">Efeito de transformação de perspectiva 3D</span><span class="sxs-lookup"><span data-stu-id="9c42f-104">3D perspective transform effect</span></span>

<span data-ttu-id="9c42f-105">Use o efeito de transformação de perspectiva 3D para girar a imagem em 3 dimensões como se fosse exibida de uma distância.</span><span class="sxs-lookup"><span data-stu-id="9c42f-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="9c42f-106">A transformação de perspectiva 3D é mais conveniente do que o efeito de transformação 3D, mas só expõe um subconjunto da funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="9c42f-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="9c42f-107">Você pode calcular uma matriz de transformação 3D completa e aplicar uma matriz de transformação mais arbitrária a uma imagem usando o efeito de [transformação 3D](3d-transform.md) .</span><span class="sxs-lookup"><span data-stu-id="9c42f-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="9c42f-108">O CLSID para esse efeito é CLSID \_ D2D13DPerspectiveTransform.</span><span class="sxs-lookup"><span data-stu-id="9c42f-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="9c42f-109">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="9c42f-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9c42f-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="9c42f-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9c42f-111">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="9c42f-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="9c42f-112">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="9c42f-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="9c42f-113">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="9c42f-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="9c42f-114">Requirements</span><span class="sxs-lookup"><span data-stu-id="9c42f-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9c42f-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c42f-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9c42f-116">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="9c42f-116">Example image</span></span>



| <span data-ttu-id="9c42f-117">Antes</span><span class="sxs-lookup"><span data-stu-id="9c42f-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)           |
| <span data-ttu-id="9c42f-119">After (após)</span><span class="sxs-lookup"><span data-stu-id="9c42f-119">After</span></span>                                                                |
| ![a imagem após o efeito.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="9c42f-121">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="9c42f-121">Effect properties</span></span>



| <span data-ttu-id="9c42f-122">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="9c42f-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="9c42f-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c42f-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c42f-124">Interpolação</span><span class="sxs-lookup"><span data-stu-id="9c42f-124">InterpolationMode</span></span><br/> <span data-ttu-id="9c42f-125">\_Modo de \_ \_ interpolação de prop d2d1 3DPERSPECTIVETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="9c42f-126">O modo de interpolação usado pelo efeito na imagem.</span><span class="sxs-lookup"><span data-stu-id="9c42f-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="9c42f-127">Há 5 modos de escala que variam de qualidade e velocidade.</span><span class="sxs-lookup"><span data-stu-id="9c42f-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="9c42f-128">O tipo é \_ o \_ modo de interpolação d2d1 3DPERSPECTIVETRANSFORM \_ .</span><span class="sxs-lookup"><span data-stu-id="9c42f-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="9c42f-129">O valor padrão é D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolação \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="9c42f-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="9c42f-130">Bordermode</span><span class="sxs-lookup"><span data-stu-id="9c42f-130">BorderMode</span></span><br/> <span data-ttu-id="9c42f-131">\_Modo de \_ borda de prop d2d1 3DPERSPECTIVETRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="9c42f-132">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="9c42f-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="9c42f-133">Consulte [modos de borda](https://www.bing.com/search?q=Border+modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9c42f-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="9c42f-134">O tipo é o \_ modo de borda d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="9c42f-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="9c42f-135">O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9c42f-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="9c42f-136">Profundidade</span><span class="sxs-lookup"><span data-stu-id="9c42f-136">Depth</span></span><br/> <span data-ttu-id="9c42f-137">\_Profundidade de \_ prop d2d1 3DPERSPECTIVETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="9c42f-138">A distância da *PerspectiveOrigin* para o plano de projeção.</span><span class="sxs-lookup"><span data-stu-id="9c42f-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="9c42f-139">O valor especificado em DIPs e deve ser maior que 0.</span><span class="sxs-lookup"><span data-stu-id="9c42f-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="9c42f-140">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="9c42f-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="9c42f-141">O valor padrão é 1000.0 f.</span><span class="sxs-lookup"><span data-stu-id="9c42f-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="9c42f-142">PerspectiveOrigin</span><span class="sxs-lookup"><span data-stu-id="9c42f-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="9c42f-143">\_Origem da \_ perspectiva de prop d2d1 3DPERSPECTIVETRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="9c42f-144">O local X e Y do visualizador na cena 3D.</span><span class="sxs-lookup"><span data-stu-id="9c42f-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="9c42f-145">Essa propriedade é um D2D1 de vetor de um \_ \_ 2F definido como: (ponto X, ponto Y).</span><span class="sxs-lookup"><span data-stu-id="9c42f-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="9c42f-146">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="9c42f-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="9c42f-147">Defina o valor Z com a propriedade *Depth* .</span><span class="sxs-lookup"><span data-stu-id="9c42f-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="9c42f-148">O tipo é o \_ vetor d2d1 \_ 2F.</span><span class="sxs-lookup"><span data-stu-id="9c42f-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="9c42f-149">O valor padrão é {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9c42f-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="9c42f-150">LocalOffset</span><span class="sxs-lookup"><span data-stu-id="9c42f-150">LocalOffset</span></span><br/> <span data-ttu-id="9c42f-151">Deslocamento local do D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="9c42f-152">Uma tradução que o efeito executa antes de girar o plano de projeção.</span><span class="sxs-lookup"><span data-stu-id="9c42f-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="9c42f-153">Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9c42f-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9c42f-154">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="9c42f-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="9c42f-155">Type é D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9c42f-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9c42f-156">O valor padrão é {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9c42f-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="9c42f-157">GlobalOffset</span><span class="sxs-lookup"><span data-stu-id="9c42f-157">GlobalOffset</span></span><br/> <span data-ttu-id="9c42f-158">Deslocamento global de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="9c42f-159">Uma tradução que o efeito executa depois de girar o plano de projeção.</span><span class="sxs-lookup"><span data-stu-id="9c42f-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="9c42f-160">Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9c42f-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9c42f-161">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="9c42f-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="9c42f-162">Type é D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9c42f-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9c42f-163">O valor padrão é {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9c42f-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="9c42f-164">RotationOrigin</span><span class="sxs-lookup"><span data-stu-id="9c42f-164">RotationOrigin</span></span><br/> <span data-ttu-id="9c42f-165">\_Origem de \_ rotação de prop d2d1 3DPERSPECTIVETRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="9c42f-166">O ponto central da rotação que o efeito executa.</span><span class="sxs-lookup"><span data-stu-id="9c42f-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="9c42f-167">Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9c42f-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9c42f-168">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="9c42f-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="9c42f-169">Type é D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9c42f-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9c42f-170">O valor padrão é {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9c42f-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="9c42f-171">Rotação</span><span class="sxs-lookup"><span data-stu-id="9c42f-171">Rotation</span></span><br/> <span data-ttu-id="9c42f-172">\_Rotação de \_ prop d2d1 3DPERSPECTIVETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="9c42f-173">Os ângulos de rotação para cada eixo.</span><span class="sxs-lookup"><span data-stu-id="9c42f-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="9c42f-174">Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9c42f-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9c42f-175">As unidades estão em graus.</span><span class="sxs-lookup"><span data-stu-id="9c42f-175">The units are in degrees.</span></span><br/> <span data-ttu-id="9c42f-176">Type é D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9c42f-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9c42f-177">O valor padrão é {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9c42f-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="9c42f-178">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="9c42f-178">Interpolation modes</span></span>



| <span data-ttu-id="9c42f-179">Enumeração</span><span class="sxs-lookup"><span data-stu-id="9c42f-179">Enumeration</span></span>                                                              | <span data-ttu-id="9c42f-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c42f-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c42f-181">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolação \_ \_ mais próximo \_</span><span class="sxs-lookup"><span data-stu-id="9c42f-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="9c42f-182">Amostra o ponto único mais próximo e o usa.</span><span class="sxs-lookup"><span data-stu-id="9c42f-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="9c42f-183">Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="9c42f-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="9c42f-184">\_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="9c42f-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="9c42f-185">Usa uma amostra de quatro pontos e uma interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="9c42f-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="9c42f-186">Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9c42f-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="9c42f-187">\_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="9c42f-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="9c42f-188">Usa um kernel cúbico de 16 amostras para interpolação.</span><span class="sxs-lookup"><span data-stu-id="9c42f-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="9c42f-189">Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9c42f-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="9c42f-190">\_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM com \_ \_ várias \_ amostras \_ lineares</span><span class="sxs-lookup"><span data-stu-id="9c42f-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="9c42f-191">Usa quatro amostras lineares em um único pixel para suavização de multialias de borda.</span><span class="sxs-lookup"><span data-stu-id="9c42f-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="9c42f-192">Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.</span><span class="sxs-lookup"><span data-stu-id="9c42f-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="9c42f-193">\_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM \_ \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="9c42f-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="9c42f-194">Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="9c42f-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="9c42f-195">Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolação \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="9c42f-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="9c42f-196">O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.</span><span class="sxs-lookup"><span data-stu-id="9c42f-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="9c42f-197">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="9c42f-197">Border modes</span></span>



| <span data-ttu-id="9c42f-198">Nome</span><span class="sxs-lookup"><span data-stu-id="9c42f-198">Name</span></span>                     | <span data-ttu-id="9c42f-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c42f-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c42f-200">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="9c42f-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="9c42f-201">O efeito preenche a imagem com pixels pretos transparentes à medida que ele interpola, resultando em uma borda suave.</span><span class="sxs-lookup"><span data-stu-id="9c42f-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="9c42f-202">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="9c42f-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="9c42f-203">O efeito coloca a saída para o tamanho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c42f-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="9c42f-204">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="9c42f-204">Output bitmap</span></span>

<span data-ttu-id="9c42f-205">O tamanho do bitmap de saída depende da matriz de transformação aplicada à imagem.</span><span class="sxs-lookup"><span data-stu-id="9c42f-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="9c42f-206">O efeito executa a operação de transformação e, em seguida, aplica uma caixa delimitadora em volta do resultado.</span><span class="sxs-lookup"><span data-stu-id="9c42f-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="9c42f-207">O bitmap de saída é o tamanho da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="9c42f-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c42f-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c42f-208">Requirements</span></span>



| <span data-ttu-id="9c42f-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c42f-209">Requirement</span></span> | <span data-ttu-id="9c42f-210">Valor</span><span class="sxs-lookup"><span data-stu-id="9c42f-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c42f-211">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c42f-211">Minimum supported client</span></span> | <span data-ttu-id="9c42f-212">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9c42f-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9c42f-213">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c42f-213">Minimum supported server</span></span> | <span data-ttu-id="9c42f-214">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9c42f-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9c42f-215">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c42f-215">Header</span></span>                   | <span data-ttu-id="9c42f-216">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="9c42f-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9c42f-217">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c42f-217">Library</span></span>                  | <span data-ttu-id="9c42f-218">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="9c42f-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9c42f-219">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c42f-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c42f-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9c42f-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

