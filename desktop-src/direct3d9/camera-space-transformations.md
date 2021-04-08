---
description: Os vértices no espaço da câmera são calculados transformando os vértices de objeto com a matriz de visualização do mundo.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformações de espaço da câmera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089238"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="3aaae-103">Transformações de espaço da câmera (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3aaae-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="3aaae-104">Os vértices no espaço da câmera são calculados transformando os vértices de objeto com a matriz de visualização do mundo.</span><span class="sxs-lookup"><span data-stu-id="3aaae-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="3aaae-105">V = V \* wvMatrix</span><span class="sxs-lookup"><span data-stu-id="3aaae-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="3aaae-106">As normais de vértice, no espaço da câmera, são calculadas transformando as normais de objeto com a transposição inversa da matriz de exibição do mundo.</span><span class="sxs-lookup"><span data-stu-id="3aaae-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="3aaae-107">A matriz de visualização do mundo poderá ou não ser ortogonal.</span><span class="sxs-lookup"><span data-stu-id="3aaae-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="3aaae-108">N = N \* (wvMatrix ⁻ ¹)<sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="3aaae-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="3aaae-109">A inversão de matrizes e a transposição de matrizes operam em uma matriz de 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="3aaae-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="3aaae-110">A multiplicação combina a normal com a parte 3 x 3 da matriz 4 x 4 resultante.</span><span class="sxs-lookup"><span data-stu-id="3aaae-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="3aaae-111">Se o estado de renderização, D3DRENDERSTATE \_ NORMALIZENORMALS for definido como **true**, os vetores normais de vértice serão normalizados após a transformação para o espaço da câmera da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3aaae-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="3aaae-112">N = norm(N)</span><span class="sxs-lookup"><span data-stu-id="3aaae-112">N = norm(N)</span></span>

<span data-ttu-id="3aaae-113">A posição da luz no espaço da câmera é calculada transformando a posição da fonte de luz com a matriz de visualização.</span><span class="sxs-lookup"><span data-stu-id="3aaae-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="3aaae-114">LP = LP \* vMatrix</span><span class="sxs-lookup"><span data-stu-id="3aaae-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="3aaae-115">A direção para a luz no espaço da câmera para uma luz direcional é calculada multiplicando a direção da fonte de luz pela matriz de visualização, normalizando e anulando o resultado.</span><span class="sxs-lookup"><span data-stu-id="3aaae-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="3aaae-116">L<sub>dir</sub> =-normal (L<sub>dir</sub> \* wvMatrix)</span><span class="sxs-lookup"><span data-stu-id="3aaae-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="3aaae-117">Para o \_ ponto D3DLIGHT e D3DLIGHT \_ , a direção para Light é calculada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3aaae-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="3aaae-118">L<sub>dir</sub> = normal (V \* LP), em que os parâmetros são definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3aaae-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="3aaae-119">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3aaae-119">Parameter</span></span>       | <span data-ttu-id="3aaae-120">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="3aaae-120">Default value</span></span> | <span data-ttu-id="3aaae-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="3aaae-121">Type</span></span>      | <span data-ttu-id="3aaae-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aaae-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="3aaae-123">F<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="3aaae-123">L<sub>dir</sub></span></span> | <span data-ttu-id="3aaae-124">N/D</span><span class="sxs-lookup"><span data-stu-id="3aaae-124">N/A</span></span>           | <span data-ttu-id="3aaae-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3aaae-125">D3DVECTOR</span></span> | <span data-ttu-id="3aaae-126">Vetor de direção do vértice de objeto à luz</span><span class="sxs-lookup"><span data-stu-id="3aaae-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="3aaae-127">V</span><span class="sxs-lookup"><span data-stu-id="3aaae-127">V</span></span>               | <span data-ttu-id="3aaae-128">N/D</span><span class="sxs-lookup"><span data-stu-id="3aaae-128">N/A</span></span>           | <span data-ttu-id="3aaae-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3aaae-129">D3DVECTOR</span></span> | <span data-ttu-id="3aaae-130">Posição do vértice no espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="3aaae-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="3aaae-131">wvMatrix</span><span class="sxs-lookup"><span data-stu-id="3aaae-131">wvMatrix</span></span>        | <span data-ttu-id="3aaae-132">Identidade</span><span class="sxs-lookup"><span data-stu-id="3aaae-132">Identity</span></span>      | <span data-ttu-id="3aaae-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="3aaae-133">D3DMATRIX</span></span> | <span data-ttu-id="3aaae-134">Matriz composta contendo as transformções de modo de exibição e mundo</span><span class="sxs-lookup"><span data-stu-id="3aaae-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="3aaae-135">N</span><span class="sxs-lookup"><span data-stu-id="3aaae-135">N</span></span>               | <span data-ttu-id="3aaae-136">N/D</span><span class="sxs-lookup"><span data-stu-id="3aaae-136">N/A</span></span>           | <span data-ttu-id="3aaae-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3aaae-137">D3DVECTOR</span></span> | <span data-ttu-id="3aaae-138">Normal de vértice</span><span class="sxs-lookup"><span data-stu-id="3aaae-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="3aaae-139">Lₚ</span><span class="sxs-lookup"><span data-stu-id="3aaae-139">Lₚ</span></span>              | <span data-ttu-id="3aaae-140">N/D</span><span class="sxs-lookup"><span data-stu-id="3aaae-140">N/A</span></span>           | <span data-ttu-id="3aaae-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3aaae-141">D3DVECTOR</span></span> | <span data-ttu-id="3aaae-142">Posição da luz no espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="3aaae-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="3aaae-143">vMatrix</span><span class="sxs-lookup"><span data-stu-id="3aaae-143">vMatrix</span></span>         | <span data-ttu-id="3aaae-144">Identidade</span><span class="sxs-lookup"><span data-stu-id="3aaae-144">Identity</span></span>      | <span data-ttu-id="3aaae-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="3aaae-145">D3DMATRIX</span></span> | <span data-ttu-id="3aaae-146">Matriz que contém a transformação de modo de exibição</span><span class="sxs-lookup"><span data-stu-id="3aaae-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="3aaae-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3aaae-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aaae-148">Matemática de iluminação</span><span class="sxs-lookup"><span data-stu-id="3aaae-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



