---
description: A iluminação ambiente fornece iluminação constante para uma cena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Iluminação de ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500997"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="2628d-103">Iluminação de ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2628d-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="2628d-104">A iluminação ambiente fornece iluminação constante para uma cena.</span><span class="sxs-lookup"><span data-stu-id="2628d-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="2628d-105">Ele destaca todos os vértices de objeto da mesma forma porque ela não depende de quaisquer outros fatores de iluminação como normais de vértice, direção da luz, posição da luz, intervalo ou atenuação.</span><span class="sxs-lookup"><span data-stu-id="2628d-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="2628d-106">É o tipo mais rápido de iluminação, mas produz os resultados menos realistas.</span><span class="sxs-lookup"><span data-stu-id="2628d-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="2628d-107">O Direct3D contém uma única propriedade de luz ambiente global que você pode usar sem criar qualquer luz.</span><span class="sxs-lookup"><span data-stu-id="2628d-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="2628d-108">Como alternativa, você pode configurar qualquer objeto de luz para fornecer iluminação ambiente.</span><span class="sxs-lookup"><span data-stu-id="2628d-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="2628d-109">A iluminação ambiente para uma cena é descrita pela seguinte equação.</span><span class="sxs-lookup"><span data-stu-id="2628d-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="2628d-110">Iluminação de ambiente = C ₐ \* \[ g ₐ + Sum (Atten<sub>eu</sub> \* ponto<sub>i</sub> \* L<sub>ia</sub>)\]</span><span class="sxs-lookup"><span data-stu-id="2628d-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="2628d-111">Em que:</span><span class="sxs-lookup"><span data-stu-id="2628d-111">Where:</span></span>



| <span data-ttu-id="2628d-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2628d-112">Parameter</span></span>         | <span data-ttu-id="2628d-113">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="2628d-113">Default value</span></span> | <span data-ttu-id="2628d-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="2628d-114">Type</span></span>          | <span data-ttu-id="2628d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2628d-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2628d-116">Cₐ</span><span class="sxs-lookup"><span data-stu-id="2628d-116">Cₐ</span></span>                | <span data-ttu-id="2628d-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2628d-117">(0,0,0,0)</span></span>     | <span data-ttu-id="2628d-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="2628d-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="2628d-119">Cor ambiente do material</span><span class="sxs-lookup"><span data-stu-id="2628d-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="2628d-120">Gₐ</span><span class="sxs-lookup"><span data-stu-id="2628d-120">Gₐ</span></span>                | <span data-ttu-id="2628d-121">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2628d-121">(0,0,0,0)</span></span>     | <span data-ttu-id="2628d-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="2628d-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="2628d-123">Cor ambiente global</span><span class="sxs-lookup"><span data-stu-id="2628d-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="2628d-124">Atten<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="2628d-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="2628d-125">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2628d-125">(0,0,0,0)</span></span>     | <span data-ttu-id="2628d-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="2628d-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="2628d-127">Atenuação de luz da luz ith.</span><span class="sxs-lookup"><span data-stu-id="2628d-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="2628d-128">Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="2628d-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="2628d-129">Ponto<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="2628d-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="2628d-130">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2628d-130">(0,0,0,0)</span></span>     | <span data-ttu-id="2628d-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2628d-131">D3DVECTOR</span></span>     | <span data-ttu-id="2628d-132">Fator de destaque da luz ith.</span><span class="sxs-lookup"><span data-stu-id="2628d-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="2628d-133">Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="2628d-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="2628d-134">Sum</span><span class="sxs-lookup"><span data-stu-id="2628d-134">sum</span></span>               | <span data-ttu-id="2628d-135">N/D</span><span class="sxs-lookup"><span data-stu-id="2628d-135">N/A</span></span>           | <span data-ttu-id="2628d-136">N/D</span><span class="sxs-lookup"><span data-stu-id="2628d-136">N/A</span></span>           | <span data-ttu-id="2628d-137">Soma da luz ambiente</span><span class="sxs-lookup"><span data-stu-id="2628d-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="2628d-138">L<sub>ia</sub></span><span class="sxs-lookup"><span data-stu-id="2628d-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="2628d-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2628d-139">(0,0,0,0)</span></span>     | <span data-ttu-id="2628d-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2628d-140">D3DVECTOR</span></span>     | <span data-ttu-id="2628d-141">Cor ambiente da luz da luz ith</span><span class="sxs-lookup"><span data-stu-id="2628d-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="2628d-142">O valor de Cₐ é:</span><span class="sxs-lookup"><span data-stu-id="2628d-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="2628d-143">Vertex color1, If AMBIENTMATERIALSOURCE = D3DMCS \_ color1 e a primeira cor de vértice é fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="2628d-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="2628d-144">Vertex color2, If AMBIENTMATERIALSOURCE = D3DMCS \_ color2, e a segunda cor de vértice é fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="2628d-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="2628d-145">cor ambiente do material.</span><span class="sxs-lookup"><span data-stu-id="2628d-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="2628d-146">Se a opção AMBIENTMATERIALSOURCE for usada e a cor do vértice não for fornecida, a cor do ambiente de material será usada.</span><span class="sxs-lookup"><span data-stu-id="2628d-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="2628d-147">Para usar a cor ambiente do material, use SetMaterial, conforme mostrado no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="2628d-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="2628d-148">Gₐ é a cor ambiente global.</span><span class="sxs-lookup"><span data-stu-id="2628d-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="2628d-149">Ele é definido usando setrenderingstate (D3DRS \_ ambiente).</span><span class="sxs-lookup"><span data-stu-id="2628d-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="2628d-150">Há uma cor ambiente global em uma cena do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2628d-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="2628d-151">Este parâmetro não está associado um objeto de luz do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2628d-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="2628d-152">L<sub>ai</sub> é a cor ambiente da luz ith na cena.</span><span class="sxs-lookup"><span data-stu-id="2628d-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="2628d-153">Cada luz do Direct3D tem um conjunto de propriedades, uma delas é a cor ambiente.</span><span class="sxs-lookup"><span data-stu-id="2628d-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="2628d-154">O termo, sum(L<sub>ai</sub>) é a soma de todas as cores ambiente na cena.</span><span class="sxs-lookup"><span data-stu-id="2628d-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="2628d-155">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2628d-155">Example</span></span>

<span data-ttu-id="2628d-156">Neste exemplo, o objeto é colorido usando a luz ambiente da cena e uma cor ambiente de material.</span><span class="sxs-lookup"><span data-stu-id="2628d-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="2628d-157">De acordo com a equação, a cor resultante para os vértices do objeto é uma combinação da cor do material e da cor da luz.</span><span class="sxs-lookup"><span data-stu-id="2628d-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="2628d-158">As duas ilustrações a seguir mostram a cor de material, que é cinza, e a cor de luz, que é vermelho brilhante.</span><span class="sxs-lookup"><span data-stu-id="2628d-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![ilustração de uma esfera cinza](images/amb1.jpg)![ilustração de uma esfera vermelha](images/lightred.jpg)

<span data-ttu-id="2628d-161">A cena resultante é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="2628d-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="2628d-162">O único objeto na cena é uma esfera.</span><span class="sxs-lookup"><span data-stu-id="2628d-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="2628d-163">A luz ambiente destaca todos os vértices do objeto com a mesma cor.</span><span class="sxs-lookup"><span data-stu-id="2628d-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="2628d-164">Não é dependente da normal de vértice ou da direção da luz.</span><span class="sxs-lookup"><span data-stu-id="2628d-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="2628d-165">Como resultado, o círculo se parece com um círculo 2D porque não há nenhuma diferença na sombreamento ao redor a superfície do objeto.</span><span class="sxs-lookup"><span data-stu-id="2628d-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![ilustração de uma esfera com iluminação](images/lighta.jpg)

<span data-ttu-id="2628d-167">Para dar uma aparência mais realista aos objetos, aplique iluminação especular ou difusa além de iluminação.</span><span class="sxs-lookup"><span data-stu-id="2628d-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2628d-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2628d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2628d-169">Matemática de iluminação</span><span class="sxs-lookup"><span data-stu-id="2628d-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



