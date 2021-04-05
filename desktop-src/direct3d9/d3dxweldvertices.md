---
description: As soldas agrupam vértices replicados que têm atributos iguais. Esse método usa valores de Épsilon especificados para comparações de igualdade.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Função D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664017"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="5f80e-104">Função D3DXWeldVertices</span><span class="sxs-lookup"><span data-stu-id="5f80e-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="5f80e-105">As soldas agrupam vértices replicados que têm atributos iguais.</span><span class="sxs-lookup"><span data-stu-id="5f80e-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="5f80e-106">Esse método usa valores de Épsilon especificados para comparações de igualdade.</span><span class="sxs-lookup"><span data-stu-id="5f80e-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f80e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f80e-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="5f80e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f80e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f80e-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5f80e-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5f80e-111">Ponteiro para um objeto [**ID3DXMesh**](id3dxmesh.md) , a malha da qual os vértices de soldagem.</span><span class="sxs-lookup"><span data-stu-id="5f80e-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="5f80e-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f80e-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f80e-114">Combinação de um ou mais sinalizadores de [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span><span class="sxs-lookup"><span data-stu-id="5f80e-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f80e-115">*pEpsilons* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-116">Tipo: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f80e-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="5f80e-117">Ponteiro para uma estrutura [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , especificando os valores de Épsilon a serem usados para esse método.</span><span class="sxs-lookup"><span data-stu-id="5f80e-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="5f80e-118">Use **NULL** para inicializar todos os membros da estrutura com um valor padrão de 1,0 e-6F.</span><span class="sxs-lookup"><span data-stu-id="5f80e-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="5f80e-119">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-120">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f80e-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5f80e-121">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de origem.</span><span class="sxs-lookup"><span data-stu-id="5f80e-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="5f80e-122">Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5f80e-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="5f80e-123">Se esse parâmetro for definido como **NULL**, [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) será chamado para criar informações de adjacência lógica.</span><span class="sxs-lookup"><span data-stu-id="5f80e-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="5f80e-124">*pAdjacencyOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f80e-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5f80e-126">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="5f80e-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="5f80e-127">Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5f80e-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="5f80e-128">*pFaceRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f80e-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5f80e-130">Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha soldada.</span><span class="sxs-lookup"><span data-stu-id="5f80e-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5f80e-131">*ppVertexRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f80e-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f80e-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f80e-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5f80e-133">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos.</span><span class="sxs-lookup"><span data-stu-id="5f80e-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="5f80e-134">Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="5f80e-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f80e-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f80e-135">Return value</span></span>

<span data-ttu-id="5f80e-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f80e-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f80e-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5f80e-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5f80e-138">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5f80e-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f80e-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f80e-139">Remarks</span></span>

<span data-ttu-id="5f80e-140">Essa função usa informações de adjacência fornecidas para determinar os pontos que são replicados.</span><span class="sxs-lookup"><span data-stu-id="5f80e-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="5f80e-141">Os vértices são mesclados com base em uma comparação de Épsilon.</span><span class="sxs-lookup"><span data-stu-id="5f80e-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="5f80e-142">Os vértices com a mesma posição já devem ter sido calculados e representados por dados de representante de ponto.</span><span class="sxs-lookup"><span data-stu-id="5f80e-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="5f80e-143">Essa função combina vértices com soldagem lógica que têm componentes semelhantes, como normalidades ou coordenadas de textura dentro de pEpsilons.</span><span class="sxs-lookup"><span data-stu-id="5f80e-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="5f80e-144">O código de exemplo a seguir chama essa função com soldagem habilitada.</span><span class="sxs-lookup"><span data-stu-id="5f80e-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="5f80e-145">Os vértices são comparados usando valores de Épsilon para a posição normal do vetor e do vértice.</span><span class="sxs-lookup"><span data-stu-id="5f80e-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="5f80e-146">Um ponteiro é retornado para uma matriz de remapeamento facial (*pFaceRemap*).</span><span class="sxs-lookup"><span data-stu-id="5f80e-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="5f80e-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f80e-147">Requirements</span></span>



| <span data-ttu-id="5f80e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f80e-148">Requirement</span></span> | <span data-ttu-id="5f80e-149">Valor</span><span class="sxs-lookup"><span data-stu-id="5f80e-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f80e-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f80e-150">Header</span></span><br/>  | <dl> <span data-ttu-id="5f80e-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f80e-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5f80e-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f80e-152">Library</span></span><br/> | <dl> <span data-ttu-id="5f80e-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f80e-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f80e-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f80e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f80e-155">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="5f80e-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
