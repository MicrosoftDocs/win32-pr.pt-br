---
description: Cria um objeto ID3DXPRTEngine que pode gerar com eficiência simulações de PRT (transferência de radiante) precomputadas de uma cena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Função D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506486"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="ee2fb-103">Função D3DXCreatePRTEngine</span><span class="sxs-lookup"><span data-stu-id="ee2fb-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="ee2fb-104">Cria um objeto [**ID3DXPRTEngine**](id3dxprtengine.md) que pode gerar com eficiência simulações de PRT (transferência de radiante) precomputadas de uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee2fb-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="ee2fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee2fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee2fb-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee2fb-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2fb-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ee2fb-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ee2fb-109">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada que modela a cena 3D.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="ee2fb-110">Essa malha deve ter uma tabela de atributos na qual os vértices estão em um atributo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ee2fb-111">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee2fb-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2fb-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee2fb-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee2fb-113">Ponteiro opcional para uma matriz de três DWORDs por face a ser preenchida com índices de face adjacentes.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="ee2fb-114">O número de bytes nessa matriz deve ser pelo menos (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="ee2fb-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="ee2fb-115">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee2fb-116">*ExtractUVs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee2fb-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2fb-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee2fb-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee2fb-118">Se **for true**, as texturas serão usadas para armazenar os vetores ALBEDOS ou PRT.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="ee2fb-119">*pBlockerMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee2fb-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2fb-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ee2fb-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ee2fb-121">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) opcional que bloqueia a cena 3D.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="ee2fb-122">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee2fb-123">*ppEngine* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ee2fb-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2fb-124">Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="ee2fb-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="ee2fb-125">Ponteiro para um objeto [**ID3DXPRTEngine**](id3dxprtengine.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee2fb-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee2fb-126">Return value</span></span>

<span data-ttu-id="ee2fb-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee2fb-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee2fb-128">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee2fb-129">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee2fb-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee2fb-130">Remarks</span></span>

<span data-ttu-id="ee2fb-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para combinar várias malhas em uma única interface de malha.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2fb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2fb-132">Requirements</span></span>



| <span data-ttu-id="ee2fb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2fb-133">Requirement</span></span> | <span data-ttu-id="ee2fb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ee2fb-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2fb-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee2fb-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ee2fb-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2fb-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ee2fb-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee2fb-137">Library</span></span><br/> | <dl> <span data-ttu-id="ee2fb-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee2fb-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee2fb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee2fb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2fb-140">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="ee2fb-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
