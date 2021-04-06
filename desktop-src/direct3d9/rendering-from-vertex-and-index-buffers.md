---
description: Os métodos de desenho indexados e não indexados têm suporte do Direct3D.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Renderização de vértices e buffers de índice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825602"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="aa7f6-103">Renderização de vértices e buffers de índice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aa7f6-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="aa7f6-104">Os métodos de desenho indexados e não indexados têm suporte do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="aa7f6-105">Os métodos indexados usam um único conjunto de índices para todos os componentes de vértice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="aa7f6-106">Os dados de vértice são armazenados em buffers de vértice, e os dados de índice são armazenados em buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="aa7f6-107">Abaixo estão listados alguns cenários comuns para desenhar primitivos usando os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="aa7f6-108">Esses exemplos comparam o uso de [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span><span class="sxs-lookup"><span data-stu-id="aa7f6-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="aa7f6-109">Cenário 1: desenhar dois triângulos sem indexação</span><span class="sxs-lookup"><span data-stu-id="aa7f6-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="aa7f6-110">Digamos que você deseja desenhar o quad que é mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![ilustração de um quadrado que consiste em dois triângulos](images/dip-fig1.png)

<span data-ttu-id="aa7f6-112">Se você usar o tipo primitivo da lista de triângulos para renderizar os dois triângulos, cada triângulo será armazenado como três vértices individuais, resultando em um buffer de vértice semelhante à ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![diagrama de um buffer de vértice que define três vértices para dois triângulos](images/dip-fig2.png)

<span data-ttu-id="aa7f6-114">A chamada de desenho é muito simples; começando no local 0 dentro do buffer de vértice, desenhe dois triângulos.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="aa7f6-115">Se a remoção estiver habilitada, a ordem dos vértices será importante.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="aa7f6-116">Este exemplo assume o estado de remoção no sentido anti-horário padrão, portanto, triângulos visíveis devem ser desenhados na ordem horária.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="aa7f6-117">O tipo primitivo da lista de triângulos simplesmente lê três vértices em ordem linear do buffer para cada triângulo, portanto, essa chamada vai desenhar triângulos (0, 1, 2) e (3, 4, 5):</span><span class="sxs-lookup"><span data-stu-id="aa7f6-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="aa7f6-118">Cenário 2: desenhar dois triângulos com indexação</span><span class="sxs-lookup"><span data-stu-id="aa7f6-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="aa7f6-119">Como você observará, o buffer de vértice contém dados duplicados nos locais 0 e 4, 2 e 5.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="aa7f6-120">Isso faz sentido porque os dois triângulos compartilham dois vértices comuns.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="aa7f6-121">Esses dados duplicados são desperdícios e o buffer de vértice pode ser compactado usando um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="aa7f6-122">Um buffer de vértice menor reduz a quantidade de dados de vértice que deve ser enviada ao adaptador gráfico.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="aa7f6-123">Ainda mais importante, usar um buffer de índice permite que o adaptador armazene vértices em um cache de vértice; Se o primitivo que está sendo desenhado contiver um vértice usado recentemente, esse vértice poderá ser buscado do cache em vez de lê-lo a partir do buffer de vértice, o que resultará em um grande aumento de desempenho.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="aa7f6-124">Um buffer de índice ' Indexes ' no buffer de vértice para que cada vértice exclusivo precise ser armazenado apenas uma vez no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="aa7f6-125">O diagrama a seguir mostra uma abordagem indexada para o cenário de desenho anterior.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![diagrama de um buffer de índice para o buffer de vértice anterior](images/dip-fig3.png)

<span data-ttu-id="aa7f6-127">O buffer de índice armazena os valores de índice do VB, que fazem referência a um vértice específico dentro do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="aa7f6-128">Um buffer de vértice pode ser considerado como uma matriz de vértices, portanto, o índice do VB é simplesmente o índice no buffer de vértice para o vértice de destino.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="aa7f6-129">Da mesma forma, um índice de IB é um índice no buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="aa7f6-130">Isso pode ficar muito confuso muito rapidamente se você não tiver cuidado. portanto, verifique se está claro no vocabulário que está sendo usado: os valores de índice do VB são indexados no buffer de vértice, os valores de índice de IB são indexados no buffer de índice, e o próprio buffer de índice armazena os valores de índice do VB.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="aa7f6-131">A chamada de desenho é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-131">The drawing call is shown below.</span></span> <span data-ttu-id="aa7f6-132">Os significados de todos os argumentos são discutidos em comprimento para o próximo cenário de desenho; por enquanto, apenas Observe que essa chamada está novamente instruindo o Direct3D a renderizar uma lista de triângulos que contém dois triangulares, começando no local 0 no buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="aa7f6-133">Essa chamada irá desenhar os mesmos dois triângulos na mesma ordem que antes, garantindo uma orientação horária adequada:</span><span class="sxs-lookup"><span data-stu-id="aa7f6-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="aa7f6-134">Cenário 3: desenhando um triângulo com indexação</span><span class="sxs-lookup"><span data-stu-id="aa7f6-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="aa7f6-135">Suponhamos agora que você deseja desenhar apenas o segundo triângulo, mas deseja usar o mesmo buffer de vértice e de índice que são usados ao desenhar todo o quad, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![diagrama do buffer de índice e buffer de vértice do segundo triângulo](images/dip-fig4.png)

<span data-ttu-id="aa7f6-137">Para essa chamada de desenho, o primeiro índice IB usado é 3; Esse valor é chamado de StartIndex.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="aa7f6-138">O menor índice do VB usado é 0; Esse valor é chamado de MinIndex.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="aa7f6-139">Embora apenas três vértices sejam requeridos para desenhar o triângulo, esses três vértices são distribuídos em quatro locais adjacentes no buffer de vértice; o número de locais dentro do bloco contíguo de memória de buffer de vértice necessário para a chamada de desenho é chamado de NumVertices e será definido como 4 nesta chamada.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="aa7f6-140">Os valores MinIndex e NumVertices são, na verdade, apenas dicas para ajudar o Direct3D a otimizar o acesso à memória durante o processamento de vértices de software e pode simplesmente ser definido para incluir todo o buffer de vértice no preço do desempenho.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="aa7f6-141">Aqui está a chamada de desenho para o caso de triângulo único; o significado do argumento BaseVertexIndex será explicado a seguir:</span><span class="sxs-lookup"><span data-stu-id="aa7f6-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="aa7f6-142">Cenário 4: desenhando um triângulo com indexação de deslocamento</span><span class="sxs-lookup"><span data-stu-id="aa7f6-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="aa7f6-143">BaseVertexIndex é um valor que é efetivamente adicionado a cada índice do VB armazenado no buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="aa7f6-144">Por exemplo, se tivéssemos passado um valor de 50 para BaseVertexIndex durante a chamada anterior, isso funcionaria como seria o mesmo que usar o buffer de índice no diagrama a seguir para a duração da chamada DrawIndexedPrimitive:</span><span class="sxs-lookup"><span data-stu-id="aa7f6-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![diagrama de um buffer de índice com um valor de 50 para BaseVertexIndex](images/dip-fig5.png)

<span data-ttu-id="aa7f6-146">Esse valor raramente é definido como algo diferente de 0, mas pode ser útil se você quiser desacoplar o buffer de índice do buffer de vértice: se ao preencher o buffer de índice para uma malha específica, o local da malha dentro do buffer de vértice ainda não é conhecido. você pode simplesmente fingir que os vértices de malha estarão localizados no início do buffer de vértice; Quando chegar a hora de fazer a chamada de desenho, basta passar o local inicial real como o BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="aa7f6-147">Essa técnica também pode ser usada ao desenhar várias instâncias de uma malha usando um único buffer de índice; por exemplo, se o buffer de vértice contiver duas malhas com ordem de desenho idêntica, mas vértices ligeiramente diferentes (talvez diferentes cores difusas ou coordenadas de textura), ambas as malhas poderiam ser desenhadas usando valores diferentes para BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="aa7f6-148">Dando um passo a esse conceito, você pode usar um buffer de índice para desenhar várias instâncias de uma malha, cada uma contida em um buffer de vértice diferente, simplesmente ligando qual buffer de vértice está ativo e ajustando o BaseVertexIndex conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="aa7f6-149">Observe que o valor BaseVertexIndex também é adicionado automaticamente ao argumento MinIndex, o que faz sentido quando você vê como ele é usado:</span><span class="sxs-lookup"><span data-stu-id="aa7f6-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="aa7f6-150">Vamos fingir que, novamente, desejamos desenhar apenas o segundo triângulo do Quad usando o mesmo buffer de índice que antes; no entanto, um buffer de vértice diferente está sendo usado no qual o quad está localizado no índice do VB 50.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="aa7f6-151">A ordem relativa dos vértices quádruplos permanece inalterada, apenas o local inicial dentro do buffer de vértice é diferente.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="aa7f6-152">O buffer de índice e o buffer de vértice se pareceriam com o diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa7f6-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![diagrama do buffer de índice e buffer de vértice com um índice vb de 50](images/dip-fig6.png)

<span data-ttu-id="aa7f6-154">Aqui está a chamada de desenho apropriada; Observe que BaseVertexIndex é o único valor que foi alterado do cenário anterior:</span><span class="sxs-lookup"><span data-stu-id="aa7f6-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="aa7f6-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa7f6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa7f6-156">Primitivos de renderização</span><span class="sxs-lookup"><span data-stu-id="aa7f6-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
