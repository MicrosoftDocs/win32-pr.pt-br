---
description: A iluminação emissive é descrita por um termo único.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Iluminação emissiva (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105798569"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="9aa1e-103">Iluminação emissiva (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9aa1e-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="9aa1e-104">A iluminação emissive é descrita por um termo único.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="9aa1e-105">Iluminação emissiva = Cₑ</span><span class="sxs-lookup"><span data-stu-id="9aa1e-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="9aa1e-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="9aa1e-106">Where:</span></span>



| <span data-ttu-id="9aa1e-107">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aa1e-107">Parameter</span></span> | <span data-ttu-id="9aa1e-108">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="9aa1e-108">Default value</span></span> | <span data-ttu-id="9aa1e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9aa1e-109">Type</span></span>          | <span data-ttu-id="9aa1e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9aa1e-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="9aa1e-111">Cₑ</span><span class="sxs-lookup"><span data-stu-id="9aa1e-111">Cₑ</span></span>        | <span data-ttu-id="9aa1e-112">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="9aa1e-112">(0,0,0,0)</span></span>     | <span data-ttu-id="9aa1e-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="9aa1e-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="9aa1e-114">Cor emissiva.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-114">Emissive color.</span></span> |



 

<span data-ttu-id="9aa1e-115">O valor de C ₑ é:</span><span class="sxs-lookup"><span data-stu-id="9aa1e-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="9aa1e-116">Vertex color1, If EMISSIVEMATERIALSOURCE = D3DMCS \_ color1 e a primeira cor de vértice é fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="9aa1e-117">Vertex color2, If EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, e a segunda cor de vértice é fornecida na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="9aa1e-118">cor do emissiva do material</span><span class="sxs-lookup"><span data-stu-id="9aa1e-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="9aa1e-119">Se a opção EMISSIVEMATERIALSOURCE for usada e a cor do vértice não for fornecida, a cor do material emissiva será usada.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="9aa1e-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9aa1e-120">Example</span></span>

<span data-ttu-id="9aa1e-121">Neste exemplo, o objeto é colorido usando a luz ambiente da cena e uma cor ambiente de material.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="9aa1e-122">O código é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="9aa1e-123">De acordo com a equação, a cor resultante para os vértices de objeto é a cor do material.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="9aa1e-124">A ilustração a seguir mostra a cor do material, que é verde.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="9aa1e-125">A luz emissiva destaca todos os vértices do objeto com a mesma cor.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="9aa1e-126">Não é dependente da normal de vértice ou da direção da luz.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="9aa1e-127">Como resultado, o círculo se parece com um círculo 2D porque não há nenhuma diferença na sombreamento ao redor a superfície do objeto.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![ilustração de uma esfera verde](images/lighte.jpg)

<span data-ttu-id="9aa1e-129">A ilustração a seguir mostra como o emissiva Light mistura com os outros três tipos de luzes, dos exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="9aa1e-130">No lado direito da esfera, há uma mistura de luz emissiva verde e luz ambiente vermelha.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="9aa1e-131">No lado esquerdo da esfera, a luz emissiva verde combina com a luz difusa e a luz ambiente vermelha, produzindo um gradiente vermelho.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="9aa1e-132">O realce especular é branco no centro e cria um anel de amarelo à medida que o valor da luz especular cai nitidamente deixando os valores de luz emissiva, difusa e ambiente se misturarem para formar o amarelo.</span><span class="sxs-lookup"><span data-stu-id="9aa1e-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![ilustração de uma esfera verde com luz emissiva](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="9aa1e-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9aa1e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa1e-135">Matemática de iluminação</span><span class="sxs-lookup"><span data-stu-id="9aa1e-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



