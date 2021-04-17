---
description: Divide uma malha em malhas menores que o tamanho especificado.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Função D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811722"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="1461a-103">Função D3DXSplitMesh</span><span class="sxs-lookup"><span data-stu-id="1461a-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="1461a-104">Divide uma malha em malhas menores que o tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="1461a-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="1461a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1461a-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="1461a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1461a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1461a-107">*pMeshIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1461a-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1461a-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1461a-109">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha de origem.</span><span class="sxs-lookup"><span data-stu-id="1461a-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-110">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1461a-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1461a-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1461a-112">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha a ser simplificada.</span><span class="sxs-lookup"><span data-stu-id="1461a-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-113">*MaxSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1461a-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-114">Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1461a-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1461a-115">Número máximo de vértices na malha resultante.</span><span class="sxs-lookup"><span data-stu-id="1461a-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-116">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1461a-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1461a-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1461a-118">Sinalizadores de opção para as novas malhas.</span><span class="sxs-lookup"><span data-stu-id="1461a-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-119">*pMeshesOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1461a-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1461a-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1461a-121">Número de malhas retornadas.</span><span class="sxs-lookup"><span data-stu-id="1461a-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-122">*ppMeshArrayOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1461a-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-123">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1461a-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1461a-124">Buffer que contém uma matriz de interfaces [**ID3DXMesh**](id3dxmesh.md) para as novas malhas.</span><span class="sxs-lookup"><span data-stu-id="1461a-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="1461a-125">Para uma malha de origem dividida em n malhas, *ppMeshArrayOut* é uma matriz de n **ID3DXMesh** ponteiros.</span><span class="sxs-lookup"><span data-stu-id="1461a-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-126">*ppAdjacencyArrayOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1461a-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1461a-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1461a-128">Buffer que contém uma matriz de matrizes de adjacência (DWORDs) para as novas malhas.</span><span class="sxs-lookup"><span data-stu-id="1461a-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="1461a-129">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1461a-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="1461a-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1461a-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-131">*ppFaceRemapArrayOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1461a-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1461a-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1461a-133">Buffer que contém uma matriz de matrizes de remapeamento facial (DWORDs) para as novas malhas.</span><span class="sxs-lookup"><span data-stu-id="1461a-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="1461a-134">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1461a-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="1461a-135">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1461a-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="1461a-136">*ppVertRemapArrayOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1461a-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1461a-137">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1461a-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1461a-138">Buffer que contém uma matriz de matrizes de remapeamento de vértice para as novas malhas.</span><span class="sxs-lookup"><span data-stu-id="1461a-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="1461a-139">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1461a-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="1461a-140">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1461a-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1461a-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1461a-141">Return value</span></span>

<span data-ttu-id="1461a-142">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1461a-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1461a-143">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1461a-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1461a-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="1461a-144">Remarks</span></span>

<span data-ttu-id="1461a-145">Um uso comum dessa função é dividir uma malha com índices de 32 bits (mais de 65535 vértices) em mais de uma malha, cada um com índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1461a-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="1461a-146">As matrizes de adjacência, remapeamento de vértice e remapeamento de face são as DWORDs em que cada matriz contém n ponteiros DWORD, seguidos pelos dados DWORD referenciados pelos ponteiros.</span><span class="sxs-lookup"><span data-stu-id="1461a-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="1461a-147">Por exemplo, para obter as informações de remapeamento facial para a face 3 na malha 2, o código a seguir pode ser usado, supondo que os dados de remapeamento facial foram retornados em uma variável chamada *ppFaceRemapArrayOut*.</span><span class="sxs-lookup"><span data-stu-id="1461a-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="1461a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1461a-148">Requirements</span></span>



| <span data-ttu-id="1461a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="1461a-149">Requirement</span></span> | <span data-ttu-id="1461a-150">Valor</span><span class="sxs-lookup"><span data-stu-id="1461a-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1461a-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1461a-151">Header</span></span><br/>  | <dl> <span data-ttu-id="1461a-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1461a-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1461a-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1461a-153">Library</span></span><br/> | <dl> <span data-ttu-id="1461a-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1461a-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1461a-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="1461a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1461a-156">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="1461a-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
