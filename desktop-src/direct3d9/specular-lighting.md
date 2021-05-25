---
description: A reflexão de modelagem especular exige que o sistema não só saiba em que direção a luz está viajando, mas também a direção para o olho do visualizador.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Iluminação especular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343671"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="0be84-103">Iluminação especular (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0be84-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="0be84-104">A reflexão de modelagem especular exige que o sistema não só saiba em que direção a luz está viajando, mas também a direção para o olho do visualizador.</span><span class="sxs-lookup"><span data-stu-id="0be84-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="0be84-105">O sistema usa uma versão simplificada do modelo de reflexo especular Phong, que utiliza um vetor de metade para aproximar a intensidade da reflexão especular.</span><span class="sxs-lookup"><span data-stu-id="0be84-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="0be84-106">O estado de iluminação padrão não calcula os realces especulares.</span><span class="sxs-lookup"><span data-stu-id="0be84-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="0be84-107">Para habilitar a iluminação especular, certifique-se de definir D3DRS \_ SPECULARENABLE como **true**.</span><span class="sxs-lookup"><span data-stu-id="0be84-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="0be84-108">Equação de Iluminação Especular</span><span class="sxs-lookup"><span data-stu-id="0be84-108">Specular Lighting Equation</span></span>

<span data-ttu-id="0be84-109">A iluminação especular é descrita pela seguinte equação:</span><span class="sxs-lookup"><span data-stu-id="0be84-109">Specular Lighting is described by the following equation:</span></span>

<span data-ttu-id="0be84-110">**Iluminação especular = cs \* Sum \[ ls \* (N · H)<sup>P</sup> \* Atten \* especial\]**</span><span class="sxs-lookup"><span data-stu-id="0be84-110">**Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span></span>



 

<span data-ttu-id="0be84-111">A tabela a seguir identifica as variáveis, seus tipos e seus intervalos.</span><span class="sxs-lookup"><span data-stu-id="0be84-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="0be84-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be84-112">Parameter</span></span>    | <span data-ttu-id="0be84-113">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="0be84-113">Default value</span></span> | <span data-ttu-id="0be84-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="0be84-114">Type</span></span>          | <span data-ttu-id="0be84-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0be84-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be84-116">Cₛ</span><span class="sxs-lookup"><span data-stu-id="0be84-116">Cₛ</span></span>           | <span data-ttu-id="0be84-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="0be84-117">(0,0,0,0)</span></span>     | <span data-ttu-id="0be84-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="0be84-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="0be84-119">Cor especular.</span><span class="sxs-lookup"><span data-stu-id="0be84-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="0be84-120">Sum</span><span class="sxs-lookup"><span data-stu-id="0be84-120">sum</span></span>          | <span data-ttu-id="0be84-121">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-121">N/A</span></span>           | <span data-ttu-id="0be84-122">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-122">N/A</span></span>           | <span data-ttu-id="0be84-123">Referência do componente especular cada da luz.</span><span class="sxs-lookup"><span data-stu-id="0be84-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="0be84-124">N</span><span class="sxs-lookup"><span data-stu-id="0be84-124">N</span></span>            | <span data-ttu-id="0be84-125">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-125">N/A</span></span>           | <span data-ttu-id="0be84-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0be84-126">D3DVECTOR</span></span>     | <span data-ttu-id="0be84-127">Normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="0be84-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="0be84-128">H</span><span class="sxs-lookup"><span data-stu-id="0be84-128">H</span></span>            | <span data-ttu-id="0be84-129">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-129">N/A</span></span>           | <span data-ttu-id="0be84-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0be84-130">D3DVECTOR</span></span>     | <span data-ttu-id="0be84-131">Vetor de metade.</span><span class="sxs-lookup"><span data-stu-id="0be84-131">Half way vector.</span></span> <span data-ttu-id="0be84-132">Consulte a seção sobre o vetor de metade.</span><span class="sxs-lookup"><span data-stu-id="0be84-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="0be84-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="0be84-133"><sup>P</sup></span></span> | <span data-ttu-id="0be84-134">0.0</span><span class="sxs-lookup"><span data-stu-id="0be84-134">0.0</span></span>           | <span data-ttu-id="0be84-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0be84-135">FLOAT</span></span>         | <span data-ttu-id="0be84-136">Potência de reflexão especular.</span><span class="sxs-lookup"><span data-stu-id="0be84-136">Specular reflection power.</span></span> <span data-ttu-id="0be84-137">Intervalo é 0 até + infinito</span><span class="sxs-lookup"><span data-stu-id="0be84-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="0be84-138">Lₛ</span><span class="sxs-lookup"><span data-stu-id="0be84-138">Lₛ</span></span>           | <span data-ttu-id="0be84-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="0be84-139">(0,0,0,0)</span></span>     | <span data-ttu-id="0be84-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="0be84-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="0be84-141">Cor especular clara.</span><span class="sxs-lookup"><span data-stu-id="0be84-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="0be84-142">Atten</span><span class="sxs-lookup"><span data-stu-id="0be84-142">Atten</span></span>        | <span data-ttu-id="0be84-143">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-143">N/A</span></span>           | <span data-ttu-id="0be84-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0be84-144">FLOAT</span></span>         | <span data-ttu-id="0be84-145">Valor de atenuação clara.</span><span class="sxs-lookup"><span data-stu-id="0be84-145">Light attenuation value.</span></span> <span data-ttu-id="0be84-146">Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="0be84-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="0be84-147">À Vista</span><span class="sxs-lookup"><span data-stu-id="0be84-147">Spot</span></span>         | <span data-ttu-id="0be84-148">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-148">N/A</span></span>           | <span data-ttu-id="0be84-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0be84-149">FLOAT</span></span>         | <span data-ttu-id="0be84-150">Fator de destaque.</span><span class="sxs-lookup"><span data-stu-id="0be84-150">Spotlight factor.</span></span> <span data-ttu-id="0be84-151">Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="0be84-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="0be84-152">O valor de Cₛ é:</span><span class="sxs-lookup"><span data-stu-id="0be84-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="0be84-153">vértice color1, se a origem do material especular for D3DMCS \_ color1 e a primeira cor de vértice for fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="0be84-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="0be84-154">vértice color2, se a origem do material especular for D3DMCS \_ color2 e a segunda cor de vértice for fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="0be84-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="0be84-155">cor especular do material</span><span class="sxs-lookup"><span data-stu-id="0be84-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="0be84-156">Se a opção fonte de material especular for usada e a cor de vértice não for fornecida, a cor especular material será usada.</span><span class="sxs-lookup"><span data-stu-id="0be84-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="0be84-157">Componentes especulares são vinculados para estar entre 0 e 255, depois que todas as luzes são processadas e interpoladas separadamente.</span><span class="sxs-lookup"><span data-stu-id="0be84-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="0be84-158">O vetor de metade</span><span class="sxs-lookup"><span data-stu-id="0be84-158">The Halfway Vector</span></span>

<span data-ttu-id="0be84-159">O vetor de metade (H) existe situado entre dois vetores: o vetor de um vértice de objeto para a fonte de luz e o vetor de um vértice de objeto para a posição da câmera.</span><span class="sxs-lookup"><span data-stu-id="0be84-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="0be84-160">O Direct3D fornece duas maneiras de calcular o vetor de metade.</span><span class="sxs-lookup"><span data-stu-id="0be84-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="0be84-161">Quando D3DRS \_ LOCALVIEWER é definido como **true**, o sistema calcula o vetor intermediário usando a posição da câmera e a posição do vértice, juntamente com o vetor de direção da luz.</span><span class="sxs-lookup"><span data-stu-id="0be84-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="0be84-162">A fórmula a seguir mostra isso.</span><span class="sxs-lookup"><span data-stu-id="0be84-162">The following formula illustrates this.</span></span>

<span data-ttu-id="0be84-163">**H = normal (normal (CP-VP) + f <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="0be84-163">**H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)**</span></span>



 



| <span data-ttu-id="0be84-164">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be84-164">Parameter</span></span>       | <span data-ttu-id="0be84-165">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="0be84-165">Default value</span></span> | <span data-ttu-id="0be84-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="0be84-166">Type</span></span>      | <span data-ttu-id="0be84-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="0be84-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="0be84-168">Cₚ</span><span class="sxs-lookup"><span data-stu-id="0be84-168">Cₚ</span></span>              | <span data-ttu-id="0be84-169">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-169">N/A</span></span>           | <span data-ttu-id="0be84-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0be84-170">D3DVECTOR</span></span> | <span data-ttu-id="0be84-171">Posição da câmera.</span><span class="sxs-lookup"><span data-stu-id="0be84-171">Camera position.</span></span>                                             |
| <span data-ttu-id="0be84-172">Vₚ</span><span class="sxs-lookup"><span data-stu-id="0be84-172">Vₚ</span></span>              | <span data-ttu-id="0be84-173">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-173">N/A</span></span>           | <span data-ttu-id="0be84-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0be84-174">D3DVECTOR</span></span> | <span data-ttu-id="0be84-175">Posição do vértice.</span><span class="sxs-lookup"><span data-stu-id="0be84-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="0be84-176">F<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="0be84-176">L<sub>dir</sub></span></span> | <span data-ttu-id="0be84-177">N/D</span><span class="sxs-lookup"><span data-stu-id="0be84-177">N/A</span></span>           | <span data-ttu-id="0be84-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0be84-178">D3DVECTOR</span></span> | <span data-ttu-id="0be84-179">Vetor de direção da posição de vértice para a posição da luz.</span><span class="sxs-lookup"><span data-stu-id="0be84-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="0be84-180">Determinar o vetor de metade dessa maneira pode ser computacionalmente intensa.</span><span class="sxs-lookup"><span data-stu-id="0be84-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="0be84-181">Como alternativa, a definição de D3DRS \_ LOCALVIEWER = **false** instrui o sistema a agir como se o ponto de vista estivesse infinitamente distante no eixo z.</span><span class="sxs-lookup"><span data-stu-id="0be84-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="0be84-182">Isso se reflete na seguinte fórmula.</span><span class="sxs-lookup"><span data-stu-id="0be84-182">This is reflected in the following formula.</span></span>

<span data-ttu-id="0be84-183">**H = normal ((0, 0, 1) + f <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="0be84-183">**H = norm((0,0,1) + L<sub>dir</sub>)**</span></span>



 

<span data-ttu-id="0be84-184">Essa configuração é computacionalmente menos intensa, mas muito menos precisa, portanto, é melhor usada por aplicativos que usam a projeção ortogonal.</span><span class="sxs-lookup"><span data-stu-id="0be84-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="0be84-185">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0be84-185">Example</span></span>

<span data-ttu-id="0be84-186">Neste exemplo, o objeto é colorido usando a cor da luz especular da cena e uma cor especular de material.</span><span class="sxs-lookup"><span data-stu-id="0be84-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="0be84-187">O código é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="0be84-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="0be84-188">De acordo com a equação, a cor resultante para os vértices do objeto é uma combinação da cor do material e da cor da luz.</span><span class="sxs-lookup"><span data-stu-id="0be84-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="0be84-189">A ilustração a seguir mostra a cor do material especular, que é cinza, e a cor da luz especular, que é branca.</span><span class="sxs-lookup"><span data-stu-id="0be84-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![ilustração de uma esfera cinza](images/amb1.jpg)![ilustração de um círculo branco](images/lightwhite.jpg)

<span data-ttu-id="0be84-192">O destaque especular resultante é mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="0be84-192">The resulting specular highlight is shown in the following illustration.</span></span>

![ilustração do realce especular](images/lights.jpg)

<span data-ttu-id="0be84-194">Combinar o realce especular com a iluminação ambiente e difusa produz a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="0be84-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="0be84-195">Com todos os três tipos de iluminação aplicada, isso mais claramente se parece com um objeto realista.</span><span class="sxs-lookup"><span data-stu-id="0be84-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![ilustração da combinação do realce especular, iluminação ambiente e iluminação difusa](images/lightads.jpg)

<span data-ttu-id="0be84-197">A iluminação especular é mais intensa para se calcular do que a iluminação difusa.</span><span class="sxs-lookup"><span data-stu-id="0be84-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="0be84-198">Ela normalmente é usada para fornecer dicas visuais sobre o material da superfície.</span><span class="sxs-lookup"><span data-stu-id="0be84-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="0be84-199">O realce especular varia em tamanho e cor com o material da superfície.</span><span class="sxs-lookup"><span data-stu-id="0be84-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0be84-200">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0be84-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be84-201">Matemática de iluminação</span><span class="sxs-lookup"><span data-stu-id="0be84-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



