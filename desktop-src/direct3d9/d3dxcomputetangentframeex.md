---
description: Executa cálculos de quadro tangente em uma malha. Os vetores tangente, binormal e opcionalmente normais são gerados. As singularidades são tratadas conforme exigido pelo agrupamento de bordas e divisão de vértices.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Função D3DXComputeTangentFrameEx (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815526"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="41043-105">Função D3DXComputeTangentFrameEx</span><span class="sxs-lookup"><span data-stu-id="41043-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="41043-106">Executa cálculos de quadro tangente em uma malha.</span><span class="sxs-lookup"><span data-stu-id="41043-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="41043-107">Os vetores tangente, binormal e opcionalmente normais são gerados.</span><span class="sxs-lookup"><span data-stu-id="41043-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="41043-108">As singularidades são tratadas conforme exigido pelo agrupamento de bordas e divisão de vértices.</span><span class="sxs-lookup"><span data-stu-id="41043-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="41043-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41043-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="41043-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41043-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41043-111">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-112">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="41043-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="41043-113">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="41043-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="41043-114">*dwTextureInSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-116">Especifica a semântica de entrada da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="41043-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="41043-117">Se D3DX \_ padrão, a função assumirá que não há coordenadas de textura e a função falhará, a menos que o cálculo de vetor normal seja especificado.</span><span class="sxs-lookup"><span data-stu-id="41043-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="41043-118">*dwTextureInIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-120">Se uma malha tiver várias coordenadas de textura, especificará a coordenada de textura a ser usada para os cálculos de quadro tangente.</span><span class="sxs-lookup"><span data-stu-id="41043-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="41043-121">Se for zero, a malha terá apenas uma única coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="41043-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="41043-122">*dwUPartialOutSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-124">Especifica a semântica de saída para o tipo, normalmente D3DDECLUSAGE \_ tangente, que descreve onde o derivativo parcial em relação à coordenada de textura U será armazenado.</span><span class="sxs-lookup"><span data-stu-id="41043-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="41043-125">Se D3DX \_ padrão, esse derivativo parcial não será armazenado.</span><span class="sxs-lookup"><span data-stu-id="41043-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="41043-126">*dwUPartialOutIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-128">Especifica o índice semântico no qual armazenar o derivativo parcial em relação à coordenada de textura de U.</span><span class="sxs-lookup"><span data-stu-id="41043-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="41043-129">*dwVPartialOutSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-131">Especifica o tipo [**D3DDECLUSAGE**](./d3ddeclusage.md) , geralmente D3DDECLUSAGE \_ binormal, que descreve onde o derivativo parcial em relação à coordenada de textura V será armazenado.</span><span class="sxs-lookup"><span data-stu-id="41043-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="41043-132">Se D3DX \_ padrão, esse derivativo parcial não será armazenado.</span><span class="sxs-lookup"><span data-stu-id="41043-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="41043-133">*dwVPartialOutIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-135">Especifica o índice semântico no qual armazenar o derivativo parcial em relação à coordenada de textura V.</span><span class="sxs-lookup"><span data-stu-id="41043-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="41043-136">*dwNormalOutSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-138">Especifica a semântica normal de saída, normalmente D3DDECLUSAGE \_ normal, que descreve onde o vetor normal em cada vértice será armazenado.</span><span class="sxs-lookup"><span data-stu-id="41043-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="41043-139">Se D3DX \_ padrão, esse vetor normal não será armazenado.</span><span class="sxs-lookup"><span data-stu-id="41043-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="41043-140">*dwNormalOutIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-141">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-142">Especifica o índice semântico no qual armazenar o vetor normal em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="41043-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="41043-143">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-145">Combinação de um ou mais sinalizadores [**D3DXTANGENT**](./d3dxtangent.md) que especificam opções de computação de quadro tangente.</span><span class="sxs-lookup"><span data-stu-id="41043-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="41043-146">Se for **NULL**, as seguintes opções serão especificadas:</span><span class="sxs-lookup"><span data-stu-id="41043-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="41043-147">Description</span><span class="sxs-lookup"><span data-stu-id="41043-147">Description</span></span>                                                                                              | <span data-ttu-id="41043-148">[**D3DXTANGENT**](./d3dxtangent.md) Valor do sinalizador</span><span class="sxs-lookup"><span data-stu-id="41043-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="41043-149">Peso o comprimento normal do vetor pelo ângulo, em radianos, entendeu-se pelas duas bordas deixando o vértice.</span><span class="sxs-lookup"><span data-stu-id="41043-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="41043-150">&! (D3DXTANGENT \_ PESO \_ pelo \_ peso de D3DXTANGENT de área \| \_ igual a \_ )</span><span class="sxs-lookup"><span data-stu-id="41043-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="41043-151">Calcular coordenadas cartesianas ortogonal de coordenadas de textura (u, v).</span><span class="sxs-lookup"><span data-stu-id="41043-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="41043-152">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="41043-152">See Remarks.</span></span>                   | <span data-ttu-id="41043-153">&! (D3DXTANGENT \_ ORTOGONALize \_ de \_ U \| D3DXTANGENT \_ ortogonalize \_ da \_ V)</span><span class="sxs-lookup"><span data-stu-id="41043-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="41043-154">As texturas não são encapsuladas nas direções u ou v</span><span class="sxs-lookup"><span data-stu-id="41043-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="41043-155">&! (D3DXTANGENT \_ CODIFICAÇÃO \_ UV)</span><span class="sxs-lookup"><span data-stu-id="41043-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="41043-156">Derivações parciais em relação às coordenadas de textura são normalizadas.</span><span class="sxs-lookup"><span data-stu-id="41043-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="41043-157">&! (D3DXTANGENT \_ Não \_ normalizar \_ parciais)</span><span class="sxs-lookup"><span data-stu-id="41043-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="41043-158">Os vértices são ordenados em uma direção no sentido anti-horário em volta de cada triângulo.</span><span class="sxs-lookup"><span data-stu-id="41043-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="41043-159">&! (D3DXTANGENT \_ PV de vento \_ )</span><span class="sxs-lookup"><span data-stu-id="41043-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="41043-160">Use vetores normais por vértice já presentes na malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="41043-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="41043-161">&! (D3DXTANGENT \_ CALCULAR \_ Normals)</span><span class="sxs-lookup"><span data-stu-id="41043-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="41043-162">Se \_ a geração \_ de D3DXTANGENT no \_ local não for definida, a malha de entrada será clonada.</span><span class="sxs-lookup"><span data-stu-id="41043-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="41043-163">Portanto, a malha original deve ter espaço suficiente para armazenar o vetor normal calculado e os dados derivados parciais.</span><span class="sxs-lookup"><span data-stu-id="41043-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="41043-164">*pdwAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-165">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="41043-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="41043-166">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="41043-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="41043-167">O número de bytes nessa matriz deve ser pelo menos 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="41043-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="41043-168">*fPartialEdgeThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-169">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-170">Especifica o cosseno máximo do ângulo no qual dois derivativos parciais são considerados incompatíveis entre si.</span><span class="sxs-lookup"><span data-stu-id="41043-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="41043-171">Se o produto de ponto da direção dos dois derivativos parciais em triângulos adjacentes for menor ou igual a esse limite, os vértices compartilhados entre esses triângulos serão divididos.</span><span class="sxs-lookup"><span data-stu-id="41043-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="41043-172">*fSingularPointThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-173">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-174">Especifica a magnitude máxima de um derivativo parcial no qual um vértice será considerado singular.</span><span class="sxs-lookup"><span data-stu-id="41043-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="41043-175">Como vários triângulos são incidentes em um ponto que têm quadros tangentes próximos, mas completamente cancelam um ao outro (como na parte superior de uma esfera), a magnitude do derivativo parcial diminuirá.</span><span class="sxs-lookup"><span data-stu-id="41043-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="41043-176">Se a magnitude for menor ou igual a esse limite, o vértice será dividido para cada triângulo que o contém.</span><span class="sxs-lookup"><span data-stu-id="41043-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="41043-177">*fNormalEdgeThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41043-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-178">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41043-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41043-179">Semelhante a fPartialEdgeThreshold, especifica o cosseno máximo do ângulo entre dois normais que é um limite além do qual os vértices compartilhados entre triângulos serão divididos.</span><span class="sxs-lookup"><span data-stu-id="41043-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="41043-180">Se o produto de ponto de dois normais for menor que o limite, os vértices compartilhados serão divididos, formando uma borda rígida entre triângulos vizinhos.</span><span class="sxs-lookup"><span data-stu-id="41043-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="41043-181">Se o produto de ponto for maior que o limite, os triângulos vizinhos terão seus normais interpolados.</span><span class="sxs-lookup"><span data-stu-id="41043-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="41043-182">*ppMeshOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="41043-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-183">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="41043-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="41043-184">Endereço de um ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de saída que recebe os dados de vetor calculados tangente, binormal e normal.</span><span class="sxs-lookup"><span data-stu-id="41043-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="41043-185">*ppVertexMapping* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="41043-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41043-186">Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="41043-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="41043-187">Endereço de um ponteiro para um objeto de buffer [**ID3DXBuffer**](id3dxbuffer.md) de saída que recebe um mapeamento de novos vértices computados por esse método para os vértices originais.</span><span class="sxs-lookup"><span data-stu-id="41043-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="41043-188">O buffer é uma matriz de DWORDs, com o tamanho da matriz definido como o número de vértices em ppMeshOut.</span><span class="sxs-lookup"><span data-stu-id="41043-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41043-189">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41043-189">Return value</span></span>

<span data-ttu-id="41043-190">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41043-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41043-191">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41043-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="41043-192">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="41043-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="41043-193">Comentários</span><span class="sxs-lookup"><span data-stu-id="41043-193">Remarks</span></span>

<span data-ttu-id="41043-194">Uma versão simplificada dessa função está disponível como [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span><span class="sxs-lookup"><span data-stu-id="41043-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="41043-195">O vetor normal calculado em cada vértice é sempre normalizado para ter comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="41043-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="41043-196">A solução mais robusta para a computação de coordenadas cartesianas ortogonal é não definir sinalizadores D3DXTANGENT \_ ortogonale \_ de \_ você e D3DXTANGENT \_ ortogonalize \_ de \_ V, de forma que as coordenadas ortogonales sejam computadas de ambas as coordenadas de textura que você e V.</span><span class="sxs-lookup"><span data-stu-id="41043-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="41043-197">No entanto, nesse caso, se u ou v for zero, a função computará coordenadas ortogonal usando D3DXTANGENT \_ ortogonalize \_ de \_ v ou D3DXTANGENT \_ ortogonalize \_ de \_ u, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="41043-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="41043-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41043-198">Requirements</span></span>



| <span data-ttu-id="41043-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="41043-199">Requirement</span></span> | <span data-ttu-id="41043-200">Valor</span><span class="sxs-lookup"><span data-stu-id="41043-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41043-201">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41043-201">Header</span></span><br/>  | <dl> <span data-ttu-id="41043-202"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="41043-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="41043-203">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41043-203">Library</span></span><br/> | <dl> <span data-ttu-id="41043-204"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41043-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41043-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="41043-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41043-206">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="41043-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="41043-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="41043-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
