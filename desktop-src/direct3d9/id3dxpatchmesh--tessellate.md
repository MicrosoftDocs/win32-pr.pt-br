---
description: Executa mosaico uniforme com base no nível de mosaico.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'Método ID3DXPatchMesh:: incluí (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750411"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="09307-103">Método ID3DXPatchMesh:: incluí</span><span class="sxs-lookup"><span data-stu-id="09307-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="09307-104">Executa mosaico uniforme com base no nível de mosaico.</span><span class="sxs-lookup"><span data-stu-id="09307-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="09307-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09307-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="09307-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09307-107">*fTessLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09307-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09307-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09307-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09307-109">Nível de mosaico.</span><span class="sxs-lookup"><span data-stu-id="09307-109">Tessellation level.</span></span> <span data-ttu-id="09307-110">Este é o número de vértices introduzidos entre os vértices existentes.</span><span class="sxs-lookup"><span data-stu-id="09307-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="09307-111">O intervalo desse parâmetro float é 0 < fTessLevel <= 32.</span><span class="sxs-lookup"><span data-stu-id="09307-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="09307-112">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09307-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09307-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="09307-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="09307-114">Malha mosaico resultante.</span><span class="sxs-lookup"><span data-stu-id="09307-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="09307-115">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="09307-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09307-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09307-116">Return value</span></span>

<span data-ttu-id="09307-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09307-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09307-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09307-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="09307-119">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="09307-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="09307-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="09307-120">Remarks</span></span>

<span data-ttu-id="09307-121">Essa função será executada com mais eficiência se a malha de patches tiver sido otimizada usando [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="09307-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09307-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09307-122">Requirements</span></span>



| <span data-ttu-id="09307-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="09307-123">Requirement</span></span> | <span data-ttu-id="09307-124">Valor</span><span class="sxs-lookup"><span data-stu-id="09307-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09307-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09307-125">Header</span></span><br/>  | <dl> <span data-ttu-id="09307-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="09307-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="09307-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09307-127">Library</span></span><br/> | <dl> <span data-ttu-id="09307-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09307-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09307-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="09307-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09307-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="09307-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
