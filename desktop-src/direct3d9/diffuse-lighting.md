---
description: Depois de ajustar a intensidade de luz para efeitos de atenuação, o mecanismo de iluminação calcula quanto da luz restante reflete de um vértice, dado o ângulo da normal do vértice e a direção da luz incidente.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Iluminação difusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087224"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="55a41-103">Iluminação difusa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="55a41-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="55a41-104">Depois de ajustar a intensidade de luz para efeitos de atenuação, o mecanismo de iluminação calcula quanto da luz restante reflete de um vértice, dado o ângulo da normal do vértice e a direção da luz incidente.</span><span class="sxs-lookup"><span data-stu-id="55a41-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="55a41-105">O mecanismo de iluminação ignora essa etapa para luzes direcionais, porque elas não são atenuadas com a distância.</span><span class="sxs-lookup"><span data-stu-id="55a41-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="55a41-106">O sistema considera dois tipos de reflexão, difusa e especular, e usa uma fórmula diferente para determinar a quantidade de luz que é refletida para cada um.</span><span class="sxs-lookup"><span data-stu-id="55a41-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="55a41-107">Depois que calcular os valores de luz refletida, o Direct3D aplica esses novos valores às propriedades de reflexão difusa e especular do material atual.</span><span class="sxs-lookup"><span data-stu-id="55a41-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="55a41-108">Os valores de cor resultantes são os componentes difusos e especulares que o rasterizador usa para produzir o sombreamento Gouraud e o realce especular.</span><span class="sxs-lookup"><span data-stu-id="55a41-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="55a41-109">A iluminação difusa é descrita pela seguinte equação.</span><span class="sxs-lookup"><span data-stu-id="55a41-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="55a41-110">Iluminação difusa = soma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* Atten \* Spot\]</span><span class="sxs-lookup"><span data-stu-id="55a41-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="55a41-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="55a41-111">Parameter</span></span>       | <span data-ttu-id="55a41-112">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="55a41-112">Default value</span></span> | <span data-ttu-id="55a41-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="55a41-113">Type</span></span>          | <span data-ttu-id="55a41-114">Description</span><span class="sxs-lookup"><span data-stu-id="55a41-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a41-115">Sum</span><span class="sxs-lookup"><span data-stu-id="55a41-115">sum</span></span>             | <span data-ttu-id="55a41-116">N/D</span><span class="sxs-lookup"><span data-stu-id="55a41-116">N/A</span></span>           | <span data-ttu-id="55a41-117">N/D</span><span class="sxs-lookup"><span data-stu-id="55a41-117">N/A</span></span>           | <span data-ttu-id="55a41-118">Referência de cada componente difuso da luz.</span><span class="sxs-lookup"><span data-stu-id="55a41-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="55a41-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="55a41-119">C<sub>d</sub></span></span>   | <span data-ttu-id="55a41-120">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="55a41-120">(0,0,0,0)</span></span>     | <span data-ttu-id="55a41-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="55a41-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="55a41-122">Cor difusa.</span><span class="sxs-lookup"><span data-stu-id="55a41-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="55a41-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="55a41-123">L<sub>d</sub></span></span>   | <span data-ttu-id="55a41-124">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="55a41-124">(0,0,0,0)</span></span>     | <span data-ttu-id="55a41-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="55a41-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="55a41-126">Cor difusa clara.</span><span class="sxs-lookup"><span data-stu-id="55a41-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="55a41-127">N</span><span class="sxs-lookup"><span data-stu-id="55a41-127">N</span></span>               | <span data-ttu-id="55a41-128">N/D</span><span class="sxs-lookup"><span data-stu-id="55a41-128">N/A</span></span>           | <span data-ttu-id="55a41-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="55a41-129">D3DVECTOR</span></span>     | <span data-ttu-id="55a41-130">Normal de vértice</span><span class="sxs-lookup"><span data-stu-id="55a41-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="55a41-131">F<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="55a41-131">L<sub>dir</sub></span></span> | <span data-ttu-id="55a41-132">N/D</span><span class="sxs-lookup"><span data-stu-id="55a41-132">N/A</span></span>           | <span data-ttu-id="55a41-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="55a41-133">D3DVECTOR</span></span>     | <span data-ttu-id="55a41-134">Vetor de direção do vértice de objeto à luz.</span><span class="sxs-lookup"><span data-stu-id="55a41-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="55a41-135">Atten</span><span class="sxs-lookup"><span data-stu-id="55a41-135">Atten</span></span>           | <span data-ttu-id="55a41-136">N/D</span><span class="sxs-lookup"><span data-stu-id="55a41-136">N/A</span></span>           | <span data-ttu-id="55a41-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="55a41-137">FLOAT</span></span>         | <span data-ttu-id="55a41-138">Atenuação de luz.</span><span class="sxs-lookup"><span data-stu-id="55a41-138">Light attenuation.</span></span> <span data-ttu-id="55a41-139">Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="55a41-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="55a41-140">À Vista</span><span class="sxs-lookup"><span data-stu-id="55a41-140">Spot</span></span>            | <span data-ttu-id="55a41-141">N/D</span><span class="sxs-lookup"><span data-stu-id="55a41-141">N/A</span></span>           | <span data-ttu-id="55a41-142">FLOAT</span><span class="sxs-lookup"><span data-stu-id="55a41-142">FLOAT</span></span>         | <span data-ttu-id="55a41-143">Fator de destaque.</span><span class="sxs-lookup"><span data-stu-id="55a41-143">Spotlight factor.</span></span> <span data-ttu-id="55a41-144">Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="55a41-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="55a41-145">O valor de C<sub>d</sub> é:</span><span class="sxs-lookup"><span data-stu-id="55a41-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="55a41-146">Vertex color1, If DIFFUSEMATERIALSOURCE = D3DMCS \_ color1 e a primeira cor de vértice é fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="55a41-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="55a41-147">Vertex color2, If DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, e a segunda cor de vértice é fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="55a41-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="55a41-148">cor difusa do material</span><span class="sxs-lookup"><span data-stu-id="55a41-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="55a41-149">Se a opção DIFFUSEMATERIALSOURCE for usada e a cor do vértice não for fornecida, a cor difusa do material será usada.</span><span class="sxs-lookup"><span data-stu-id="55a41-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="55a41-150">Para calcular a atenuação (Atten) ou as características de destaque (spot), veja [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="55a41-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="55a41-151">Componentes difusos são vinculados para estar entre 0 e 255, depois que todas as luzes são processadas e interpoladas separadamente.</span><span class="sxs-lookup"><span data-stu-id="55a41-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="55a41-152">O valor de iluminação difusa resultante é uma combinação dos valores de luz ambiente, difusa e emissiva.</span><span class="sxs-lookup"><span data-stu-id="55a41-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="55a41-153">Exemplo</span><span class="sxs-lookup"><span data-stu-id="55a41-153">Example</span></span>

<span data-ttu-id="55a41-154">Neste exemplo, o objeto é colorido usando a cor difusa clara e uma cor difusa de material.</span><span class="sxs-lookup"><span data-stu-id="55a41-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="55a41-155">O código é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="55a41-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="55a41-156">De acordo com a equação, a cor resultante para os vértices do objeto é uma combinação da cor do material e da cor da luz.</span><span class="sxs-lookup"><span data-stu-id="55a41-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="55a41-157">As duas ilustrações a seguir mostram a cor de material, que é cinza, e a cor de luz, que é vermelho brilhante.</span><span class="sxs-lookup"><span data-stu-id="55a41-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![ilustração de uma esfera cinza](images/amb1.jpg)![ilustração de uma esfera vermelha](images/lightred.jpg)

<span data-ttu-id="55a41-160">A cena resultante é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="55a41-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="55a41-161">O único objeto na cena é uma esfera.</span><span class="sxs-lookup"><span data-stu-id="55a41-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="55a41-162">O cálculo de iluminação difusa considera a cor difusa da luz e do material e a modifica pelo ângulo entre a direção da luz e a normal do vértice usando o produto de ponto.</span><span class="sxs-lookup"><span data-stu-id="55a41-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="55a41-163">Como resultado, o verso da esfera obtém fica escuro à medida que a superfície das curvas da esfera se afasta da luz.</span><span class="sxs-lookup"><span data-stu-id="55a41-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![ilustração de uma esfera com iluminação difusa](images/lightd.jpg)

<span data-ttu-id="55a41-165">Combinar a iluminação difusa com a iluminação ambiente dos exemplos anteriores sobreará toda a superfície do objeto.</span><span class="sxs-lookup"><span data-stu-id="55a41-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="55a41-166">A luz ambiente sombreia toda a superfície e a luz difusa ajuda a revelar a forma do objeto 3D, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="55a41-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![Ilustração de uma esfera com iluminação difusa e iluminação ambiente](images/lightad.jpg)

<span data-ttu-id="55a41-168">A iluminação difusa é mais intensa para se calcular do que a iluminação ambiente.</span><span class="sxs-lookup"><span data-stu-id="55a41-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="55a41-169">Como ela depende das normais de vértice e da direção da luz, você pode ver a geometria de objetos no espaço 3D, o que produz uma iluminação mais realística do que a iluminação ambiente.</span><span class="sxs-lookup"><span data-stu-id="55a41-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="55a41-170">Você pode usar realces especulares para obter uma aparência mais realista.</span><span class="sxs-lookup"><span data-stu-id="55a41-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55a41-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55a41-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a41-172">Matemática de iluminação</span><span class="sxs-lookup"><span data-stu-id="55a41-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



