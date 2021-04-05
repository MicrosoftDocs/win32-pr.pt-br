---
description: O Direct3D permite que um aplicativo aumente o realm de seus bastidores ao renderizar objetos Polygons segmentados – especialmente caracteres-que têm junções mescladas suavemente.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Combinação de geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645620"
---
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="5eda0-103">Combinação de geometria (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5eda0-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="5eda0-104">O Direct3D permite que um aplicativo aumente o realm de seus bastidores ao renderizar objetos Polygons segmentados – especialmente caracteres-que têm junções mescladas suavemente.</span><span class="sxs-lookup"><span data-stu-id="5eda0-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="5eda0-105">Esses efeitos são geralmente chamados de aparência.</span><span class="sxs-lookup"><span data-stu-id="5eda0-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="5eda0-106">O sistema alcança esse efeito aplicando matrizes de transformação mundiais adicionais a um único conjunto de vértices para criar vários resultados e, em seguida, executar uma combinação linear entre os vértices resultantes para criar um único conjunto de geometria para renderização.</span><span class="sxs-lookup"><span data-stu-id="5eda0-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="5eda0-107">A ilustração a seguir de um banana mostra esse processo.</span><span class="sxs-lookup"><span data-stu-id="5eda0-107">The following illustration of a banana shows this process.</span></span>

![ilustração do processo para misturar dois objetos com a textura banana](images/geometry-blend.png)

<span data-ttu-id="5eda0-109">A ilustração anterior mostra como você pode imaginar o processo de mesclagem de geometria.</span><span class="sxs-lookup"><span data-stu-id="5eda0-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="5eda0-110">Em uma única chamada de renderização, o sistema usa os vértices para o banana, transforma-os duas vezes uma vez sem modificação e uma vez com uma rotação simples e mistura os resultados para criar um banana torto.</span><span class="sxs-lookup"><span data-stu-id="5eda0-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="5eda0-111">O sistema mescla a posição do vértice, bem como o vértice normal quando a iluminação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="5eda0-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="5eda0-112">Os aplicativos não estão limitados a dois caminhos de mesclagem; O Direct3D pode misturar geometria entre até quatro matrizes mundiais, incluindo a matriz mundial padrão, [**D3DTS \_ World**](d3dts-world.md).</span><span class="sxs-lookup"><span data-stu-id="5eda0-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="5eda0-113">Quando a iluminação está habilitada, os Normals de vértice são transformados por uma matriz inversa de exibição mundial correspondente, ponderada da mesma maneira que os cálculos de posição de vértice.</span><span class="sxs-lookup"><span data-stu-id="5eda0-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="5eda0-114">O sistema normaliza o vetor normal resultante se o estado de \_ RENDERIZAÇÃO D3DRS NORMALIZENORMALS for definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="5eda0-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="5eda0-115">Sem a combinação de geometria, os modelos articulados dinâmicos geralmente são renderizados em segmentos.</span><span class="sxs-lookup"><span data-stu-id="5eda0-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="5eda0-116">Por exemplo, considere um modelo 3D do braço humano.</span><span class="sxs-lookup"><span data-stu-id="5eda0-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="5eda0-117">Na exibição mais simples, um ARM tem duas partes: o braço superior que se conecta ao corpo e o braço inferior, que se conecta à mão.</span><span class="sxs-lookup"><span data-stu-id="5eda0-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="5eda0-118">Os dois são conectados no cotovelo e o braço inferior gira nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="5eda0-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="5eda0-119">Um aplicativo que renderiza um ARM pode reter dados de vértice para o braço superior e inferior, cada um com uma matriz de transformação do mundo separada.</span><span class="sxs-lookup"><span data-stu-id="5eda0-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="5eda0-120">O exemplo de código a seguir ilustra isso.</span><span class="sxs-lookup"><span data-stu-id="5eda0-120">The following code example illustrates this.</span></span>


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



<span data-ttu-id="5eda0-121">Para renderizar o ARM, são feitas duas chamadas de renderização, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="5eda0-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



<span data-ttu-id="5eda0-122">A ilustração a seguir é um banana, modificado para usar essa técnica.</span><span class="sxs-lookup"><span data-stu-id="5eda0-122">The following illustration is a banana, modified to use this technique.</span></span>

![ilustração de um banana combinado sem mesclagem de geometria](images/noblend.png)

<span data-ttu-id="5eda0-124">As diferenças entre a geometria combinada e a geometria não misturada são óbvias.</span><span class="sxs-lookup"><span data-stu-id="5eda0-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="5eda0-125">Este exemplo é um pouco extremo.</span><span class="sxs-lookup"><span data-stu-id="5eda0-125">This example is somewhat extreme.</span></span> <span data-ttu-id="5eda0-126">Em um aplicativo do mundo real, as junções de modelos segmentados são projetadas para que as emendas não sejam tão óbvias.</span><span class="sxs-lookup"><span data-stu-id="5eda0-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="5eda0-127">No entanto, as emendas são visíveis às vezes, o que apresenta desafios constantes para designers de modelos.</span><span class="sxs-lookup"><span data-stu-id="5eda0-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="5eda0-128">A combinação de geometria no Direct3D apresenta uma alternativa ao cenário de modelagem segmentada clássica.</span><span class="sxs-lookup"><span data-stu-id="5eda0-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="5eda0-129">No entanto, a melhor qualidade visual dos objetos segmentados é o custo dos cálculos de mesclagem durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="5eda0-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="5eda0-130">Para minimizar o impacto dessas operações adicionais, o pipeline do Direct3D Geometry é otimizado para misturar geometria com a menor sobrecarga possível.</span><span class="sxs-lookup"><span data-stu-id="5eda0-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="5eda0-131">Os aplicativos que usam de forma inteligente os serviços de combinação de geometria oferecidos pelo Direct3D podem melhorar o realm de seus caracteres e, ao mesmo tempo, evitar repercussões de desempenho graves.</span><span class="sxs-lookup"><span data-stu-id="5eda0-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="5eda0-132">Mesclando Estados de transformação e de renderização</span><span class="sxs-lookup"><span data-stu-id="5eda0-132">Blending Transform and Render States</span></span>

<span data-ttu-id="5eda0-133">O método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) reconhece as macros do [**D3DTS \_ World**](d3dts-world.md) e do [**D3DTS \_ worldn**](d3dts-worldn.md) , que correspondem aos valores que podem ser definidos pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="5eda0-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="5eda0-134">Essas macros são usadas para identificar as matrizes entre as quais a geometria será mesclada.</span><span class="sxs-lookup"><span data-stu-id="5eda0-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="5eda0-135">O tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) inclui o \_ estado de renderização D3DRS VERTEXBLEND para habilitar e controlar a combinação de geometria.</span><span class="sxs-lookup"><span data-stu-id="5eda0-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="5eda0-136">Os valores válidos para esse estado de renderização são definidos pelo tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="5eda0-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="5eda0-137">Se a combinação de geometria estiver habilitada, o formato de vértice deverá incluir o número apropriado de pesos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5eda0-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="5eda0-138">Pesos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="5eda0-138">Blending Weights</span></span>

<span data-ttu-id="5eda0-139">Um peso de mesclagem, às vezes chamado de peso beta, controla a extensão até a qual uma determinada matriz do mundo afeta um vértice.</span><span class="sxs-lookup"><span data-stu-id="5eda0-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="5eda0-140">Os pesos de mesclagem são valores de ponto flutuante que variam de 0,0 a 1,0, codificados no formato de vértice, em que um valor de 0,0 significa que o vértice não é mesclado com essa matriz e 1,0 significa que o vértice é afetado de forma completa pela matriz.</span><span class="sxs-lookup"><span data-stu-id="5eda0-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="5eda0-141">Os pesos de mesclagem de geometria são codificados no formato de vértice, aparecendo imediatamente após a posição de cada vértice, conforme descrito em [códigos de FVF de função fixas (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5eda0-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="5eda0-142">Você comunica o número de pesos de mesclagem no formato de vértice, incluindo uma das [constantes FVF](d3dfvf.md) na descrição de vértice que você fornece aos métodos de renderização.</span><span class="sxs-lookup"><span data-stu-id="5eda0-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="5eda0-143">O sistema executa uma combinação linear entre os resultados ponderados das matrizes de mistura.</span><span class="sxs-lookup"><span data-stu-id="5eda0-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="5eda0-144">A equação a seguir é a fórmula de mesclagem completa.</span><span class="sxs-lookup"><span data-stu-id="5eda0-144">The following equation is the complete blending formula.</span></span>

![equação de mesclagem linear, usando matrizes de transformação mundiais](images/vert-blend-formula.png)

<span data-ttu-id="5eda0-146">Na equação anterior, vBlend é o vértice de saída, os elementos v são os vértices produzidos pela matriz mundial aplicada ([**D3DTS \_ worldn**](d3dts-worldn.md)).</span><span class="sxs-lookup"><span data-stu-id="5eda0-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="5eda0-147">Os elementos W são os valores de peso correspondentes dentro do formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="5eda0-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="5eda0-148">Um vértice misturado entre as matrizes n pode ter-1 valores de peso de mesclagem, um para cada matriz de mesclagem, exceto o último.</span><span class="sxs-lookup"><span data-stu-id="5eda0-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="5eda0-149">O sistema gera automaticamente o peso para a última matriz mundial para que a soma de todos os pesos seja 1,0, expressa na notação Sigma aqui.</span><span class="sxs-lookup"><span data-stu-id="5eda0-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="5eda0-150">Essa fórmula pode ser simplificada para cada um dos casos com suporte do Direct3D, que é mostrado nas equações a seguir.</span><span class="sxs-lookup"><span data-stu-id="5eda0-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![equações de mesclagem linear para três casos de mesclagem](images/vert-blend-formulas-simple.png)

<span data-ttu-id="5eda0-152">Essas são as formas simplificadas da fórmula de mesclagem completa para os dois, três e quatro casos de matriz de mistura.</span><span class="sxs-lookup"><span data-stu-id="5eda0-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="5eda0-153">Embora o Direct3D inclua descritores de FVF para definir vértices que contêm até cinco pesos de mesclagem, somente três podem ser usados nesta versão do DirectX.</span><span class="sxs-lookup"><span data-stu-id="5eda0-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="5eda0-154">Informações adicionais estão contidas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5eda0-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="5eda0-155">Usando a combinação de geometria (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5eda0-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="5eda0-156">Mistura de vértices indexados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5eda0-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="5eda0-157">Interpolação de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5eda0-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="5eda0-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5eda0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eda0-159">Pipeline de vértice</span><span class="sxs-lookup"><span data-stu-id="5eda0-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
