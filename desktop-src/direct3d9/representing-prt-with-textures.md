---
description: O exemplo PRTDemo e o simulador PRTCmdLine incluídos no SDK do DirectX representam vetores de transferência nos vértices de uma malha.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Representando o PRT com texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163855"
---
# <a name="representing-prt-with-textures-direct3d-9"></a><span data-ttu-id="9f478-103">Representando o PRT com texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9f478-103">Representing PRT With Textures (Direct3D 9)</span></span>

<span data-ttu-id="9f478-104">O exemplo PRTDemo e o simulador PRTCmdLine incluídos no SDK do DirectX representam vetores de transferência nos vértices de uma malha.</span><span class="sxs-lookup"><span data-stu-id="9f478-104">The PRTDemo sample and PRTCmdLine simulator included in the DirectX SDK represent transfer vectors at the vertices of a mesh.</span></span> <span data-ttu-id="9f478-105">Para representar o sinal de PRT com precisão, isso pode exigir mosaicos que podem ser impraticável para jogos atuais.</span><span class="sxs-lookup"><span data-stu-id="9f478-105">In order to represent the PRT signal accurately, this can require tessellations that may be impractical for current games.</span></span> <span data-ttu-id="9f478-106">Representar vetores de transferência em mapas de textura é uma abordagem alternativa que tem o mesmo custo de dados independente da complexidade da malha.</span><span class="sxs-lookup"><span data-stu-id="9f478-106">Representing transfer vectors in texture maps is an alternative approach that has the same data cost independent of mesh complexity.</span></span> <span data-ttu-id="9f478-107">Há várias maneiras de gerar mapas de textura de vetor de transferência usando a biblioteca D3DX PRT.</span><span class="sxs-lookup"><span data-stu-id="9f478-107">There are several ways to generate transfer vector texture maps using the D3DX PRT Library.</span></span>

## <a name="precomputing-transfer-vectors"></a><span data-ttu-id="9f478-108">Computação de vetores de transferência</span><span class="sxs-lookup"><span data-stu-id="9f478-108">Precomputing Transfer Vectors</span></span>

<span data-ttu-id="9f478-109">Uma abordagem seria modificar os exemplos de PRTDemo e PRTCmdLine para calcular um vetor de transferência a cada Texel em uma parametrização de uma superfície.</span><span class="sxs-lookup"><span data-stu-id="9f478-109">One approach would be to modify the PRTDemo and PRTCmdLine samples to compute a transfer vector at every texel in a parameterization of a surface.</span></span> <span data-ttu-id="9f478-110">Para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="9f478-110">To do this:</span></span>

1.  <span data-ttu-id="9f478-111">Modifique a chamada para [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para extrair coordenadas de textura da malha (ExtractUVs deve ser **true**)</span><span class="sxs-lookup"><span data-stu-id="9f478-111">Modify the call to [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to extract texture coordinates from the mesh (ExtractUVs must be **TRUE**)</span></span>
2.  <span data-ttu-id="9f478-112">Substitua chamadas [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) com [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) usando o mesmo tamanho de textura.</span><span class="sxs-lookup"><span data-stu-id="9f478-112">Replace [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) calls with [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) using the same texture size.</span></span>

<span data-ttu-id="9f478-113">Todos os métodos ID3DXPRTEngine funcionam com simulações por Texel, exceto para: ComputeBounceAdaptive, ComputeSSAdaptive, Computess e ComputeDirectLightingSHAdaptive.</span><span class="sxs-lookup"><span data-stu-id="9f478-113">All ID3DXPRTEngine methods work with per-texel simulations except for: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS, and ComputeDirectLightingSHAdaptive.</span></span> <span data-ttu-id="9f478-114">Embora a simulação de espaço de textura gere o resultado correto, ela geralmente pode ser razoavelmente lenta, já que provavelmente estará computando os vetores de transferência em uma alta densidade.</span><span class="sxs-lookup"><span data-stu-id="9f478-114">While texture-space simulation will generate the correct result, it can often be fairly slow since it will most likely be computing transfer vectors at a high density.</span></span>

<span data-ttu-id="9f478-115">Outra abordagem é computar uma simulação de PRT adaptável por vértice (com coordenadas de textura que serão usadas para os dados por Texel) e, em seguida, chamar [**ID3DXPRTEngine:: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (usando um buffer de saída criado usando [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) na resolução apropriada).</span><span class="sxs-lookup"><span data-stu-id="9f478-115">Another approach is to compute an adaptive per-vertex PRT simulation (with texture coordinates that will be used for the per-texel data) and then call [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (using an output buffer created using [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) at the appropriate resolution).</span></span> <span data-ttu-id="9f478-116">Isso funciona com toda a funcionalidade de PRT D3DX no SDK e, muitas vezes, pode ser muito mais eficiente do que a computação direta de um buffer de transferência por Texel.</span><span class="sxs-lookup"><span data-stu-id="9f478-116">This works with all D3DX PRT functionality in the SDK and can often be much more efficient than directly computing a per-texel transfer buffer.</span></span>

## <a name="runtime-calculations"></a><span data-ttu-id="9f478-117">Cálculos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="9f478-117">Runtime Calculations</span></span>

<span data-ttu-id="9f478-118">Se um único cluster for usado, os resultados poderão ser filtrados e não mapeados de MIP como qualquer outra textura e o sombreador de pixel será idêntico ao código do sombreador de vértice fornecido com PRTDemo.</span><span class="sxs-lookup"><span data-stu-id="9f478-118">If a single cluster is used the results can be filtered and mip-mapped like any other texture and the pixel shader is identical to the vertex shader code that ships with PRTDemo.</span></span>

<span data-ttu-id="9f478-119">Se a compactação gerar vários clusters, você não poderá filtrar ou mipmapr os dados porque os índices de clustering não são contínuos.</span><span class="sxs-lookup"><span data-stu-id="9f478-119">If compression generates multiple clusters, you cannot filter or mipmap the data because clustering indexes are not continuous.</span></span> <span data-ttu-id="9f478-120">Aqui estão algumas alternativas para lidar com dados de vários clusters:</span><span class="sxs-lookup"><span data-stu-id="9f478-120">Here are some alternatives for handling multi-clustered data:</span></span>

-   <span data-ttu-id="9f478-121">Faça toda a filtragem no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9f478-121">Do all of the filtering yourself in the pixel shader.</span></span> <span data-ttu-id="9f478-122">Infelizmente, isso geralmente não é prático por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9f478-122">Unfortunately, this is generally impractical for performance reasons.</span></span>
-   <span data-ttu-id="9f478-123">Se as texturas forem texturas não incluídas em baixa resolução (isto é, mapas de luz), é mais provável que seja mais eficiente apenas calcular a iluminação diretamente no espaço de textura, onde não ocorrerá nenhuma filtragem e renderizar o objeto com uma textura sombreada.</span><span class="sxs-lookup"><span data-stu-id="9f478-123">If the textures are low resolution non mip-mapped textures (ie: light maps), it is most likely more efficient to just compute the lighting directly in texture space - where no filtering will occur, and render the object with a shaded texture.</span></span> <span data-ttu-id="9f478-124">Isso é essencialmente um mapa claro dinâmico que é criado inteiramente na GPU.</span><span class="sxs-lookup"><span data-stu-id="9f478-124">This is essentially a dynamic light map that is created entirely on the GPU.</span></span>
-   <span data-ttu-id="9f478-125">Se um Atlas de textura for usado (consulte [usando o UVAtlas (Direct3D 9)](using-uvatlas.md)), você poderá clusterizar manualmente a cena fazendo com que todos os vetores de transferência em um componente conectado no espaço de textura estejam no mesmo cluster.</span><span class="sxs-lookup"><span data-stu-id="9f478-125">If a texture atlas is used (see [Using UVAtlas (Direct3D 9)](using-uvatlas.md)), you could manually cluster the scene by having all transfer vectors in a connected component in texture space be in the same cluster.</span></span> <span data-ttu-id="9f478-126">Dessa forma, você pode filtrar a textura porque todas as texels acessadas estaria no mesmo cluster por meio da construção.</span><span class="sxs-lookup"><span data-stu-id="9f478-126">This way you can filter the texture because all texels accessed would be in the same cluster by construction.</span></span> <span data-ttu-id="9f478-127">A ID do cluster para uma face determinada pode ser propagada a partir do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9f478-127">The cluster ID for a given face could be propagated from the vertex shader.</span></span>

<span data-ttu-id="9f478-128">Os sombreadores de pixel têm muito menos registros constantes que não podem ser indexados, portanto, o sombreador de pixel é um pouco diferente do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9f478-128">Pixel shaders have much fewer constant registers that cannot be indexed, so the pixel shader is somewhat different than the vertex shader.</span></span> <span data-ttu-id="9f478-129">Armazenar o trabalho por cluster em uma textura dinâmica de baixa resolução e usar cargas de textura seria a maneira mais eficiente de renderizar ao usar vários clusters.</span><span class="sxs-lookup"><span data-stu-id="9f478-129">Storing the per-cluster work in a low resolution dynamic texture and using texture loads would be the most efficient way to render when using multiple clusters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f478-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f478-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f478-131">Transferência de radiante preputada</span><span class="sxs-lookup"><span data-stu-id="9f478-131">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> <dt>

<span data-ttu-id="9f478-132">[Exemplo de demonstração de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9f478-132">[PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span></span>
</dt> <dt>

<span data-ttu-id="9f478-133">[Simulador de PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9f478-133">[PRT Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 



