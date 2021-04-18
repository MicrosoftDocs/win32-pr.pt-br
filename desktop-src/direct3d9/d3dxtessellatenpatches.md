---
description: Tessellates a malha determinada usando o esquema de mosaico de N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Função D3DXTessellateNPatches (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789405"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="31620-103">Função D3DXTessellateNPatches</span><span class="sxs-lookup"><span data-stu-id="31620-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="31620-104">Tessellates a malha determinada usando o esquema de mosaico de N-patch.</span><span class="sxs-lookup"><span data-stu-id="31620-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="31620-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31620-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="31620-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31620-107">*pMeshIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31620-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31620-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="31620-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="31620-109">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha para incluí.</span><span class="sxs-lookup"><span data-stu-id="31620-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="31620-110">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31620-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31620-111">Tipo: **CONST const DWORD \***</span><span class="sxs-lookup"><span data-stu-id="31620-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="31620-112">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de origem.</span><span class="sxs-lookup"><span data-stu-id="31620-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="31620-113">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="31620-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="31620-114">*NumSegs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31620-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31620-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31620-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31620-116">Número de segmentos por borda para incluí.</span><span class="sxs-lookup"><span data-stu-id="31620-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="31620-117">*QuadraticInterpNormals* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31620-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31620-118">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31620-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31620-119">Defina como **true** para usar a interpolação quadrática para Normals; Defina como **false** para interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="31620-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="31620-120">*ppMeshOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31620-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31620-121">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="31620-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="31620-122">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha mosaico retornada.</span><span class="sxs-lookup"><span data-stu-id="31620-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="31620-123">*ppAdjacencyOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31620-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31620-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="31620-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="31620-125">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="31620-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="31620-126">Se o valor desse parâmetro não for definido como **NULL**, esse buffer conterá uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de saída.</span><span class="sxs-lookup"><span data-stu-id="31620-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="31620-127">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="31620-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31620-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31620-128">Return value</span></span>

<span data-ttu-id="31620-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31620-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31620-130">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31620-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31620-131">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="31620-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="31620-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="31620-132">Remarks</span></span>

<span data-ttu-id="31620-133">Essa função tessellates usando o algoritmo N-patch.</span><span class="sxs-lookup"><span data-stu-id="31620-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="31620-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31620-134">Requirements</span></span>



| <span data-ttu-id="31620-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="31620-135">Requirement</span></span> | <span data-ttu-id="31620-136">Valor</span><span class="sxs-lookup"><span data-stu-id="31620-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31620-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31620-137">Header</span></span><br/>  | <dl> <span data-ttu-id="31620-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31620-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="31620-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31620-139">Library</span></span><br/> | <dl> <span data-ttu-id="31620-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31620-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31620-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="31620-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31620-142">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="31620-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
