---
description: A mesclagem de vértices indexados estende o suporte de mistura de vértice no Direct3D para permitir que as matrizes sejam usadas para mesclagem.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Mistura de vértices indexados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456373"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="6f3ef-103">Mistura de vértices indexados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6f3ef-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="6f3ef-104">A mesclagem de vértices indexados estende o suporte de mistura de vértice no Direct3D para permitir que as matrizes sejam usadas para mesclagem.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="6f3ef-105">Essas matrizes são referenciadas usando um índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="6f3ef-106">Esses índices são fornecidos por vértice e se referem a uma paleta de até 256 matrizes.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="6f3ef-107">Cada índice é de 8 bits e cada vértice pode ter até quatro índices, o que permite que quatro matrizes sejam mescladas por vértice.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="6f3ef-108">Os índices são empacotados em um DWORD.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="6f3ef-109">Como os índices são especificados por vértice, até 12 matrizes podem afetar um único triângulo, e qualquer matriz na paleta pode afetar os vértices de uma chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="6f3ef-110">Essa abordagem tem as seguintes vantagens.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="6f3ef-111">Ele permite que mais matrizes afetem um único triângulo.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="6f3ef-112">Ele permite que triângulos mais misturados sejam passados na mesma chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="6f3ef-113">Ele faz a mesclagem de vértice independente de índices de triângulo.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="6f3ef-114">Isso permite que malhas progressivas funcionem em conjunto com a mistura de vértice.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="6f3ef-115">Uma desvantagem dessa abordagem é que ela não funciona com primitivas de superfície curvada quando o mosaico ocorre antes do processamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="6f3ef-116">O diagrama a seguir demonstra como quatro matrizes podem afetar um vértice.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="6f3ef-117">Cada vértice tem até quatro índices, de modo que quatro matrizes podem ser mescladas por vértice.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="6f3ef-118">O diagrama usa as matrizes indexadas em 0, 2, 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![diagrama de mesclagem de vértice indexado usando 4 de 256 matrizes disponíveis](images/dword1.png)

<span data-ttu-id="6f3ef-120">O diagrama a seguir demonstra como até 12 matrizes podem afetar um triângulo.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="6f3ef-121">Usando índices especificados em uma base por vértice, até 12 matrizes podem afetar o triângulo.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![diagrama de mesclagem de vértice indexado para um triângulo usando 12 de 256 matrizes disponíveis](images/dword2.png)

<span data-ttu-id="6f3ef-123">A equação a seguir determina o caso geral de como as matrizes afetam um vértice.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![equação da mistura de vértices indexados](images/indexedvblend.png)

<span data-ttu-id="6f3ef-125">O <sub>modelo</sub> V é a posição de vértice do espaço do modelo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="6f3ef-126">Index0.. Index3 são os índices de matriz por vértice empacotados em um DWORD.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="6f3ef-127">M \[ \] é a matriz de matrizes mundiais que são indexadas no.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="6f3ef-128">b ₀.. b ₂ são os pesos de mistura.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="6f3ef-129">O<sub>mundo</sub> V é a posição de vértice do espaço do mundo de saída.</span><span class="sxs-lookup"><span data-stu-id="6f3ef-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="6f3ef-130">Para obter mais informações sobre a mistura de vértices indexados, consulte [usando o Direct3D 9](using-indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="6f3ef-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f3ef-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f3ef-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f3ef-132">Mesclagem de geometria</span><span class="sxs-lookup"><span data-stu-id="6f3ef-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



