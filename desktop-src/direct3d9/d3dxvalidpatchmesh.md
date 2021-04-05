---
description: Valida uma malha de patch, retornando o número de vértices e patches de degeneração.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Função D3DXValidPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930575"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="b2bc5-103">Função D3DXValidPatchMesh</span><span class="sxs-lookup"><span data-stu-id="b2bc5-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="b2bc5-104">Valida uma malha de patch, retornando o número de vértices e patches de degeneração.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2bc5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2bc5-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="b2bc5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2bc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2bc5-107">*pMeshIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2bc5-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2bc5-108">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b2bc5-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="b2bc5-109">Ponteiro para uma interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) , representando a malha de patch a ser testada.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="b2bc5-110">*pNumDegenerateVertices* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b2bc5-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2bc5-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2bc5-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b2bc5-112">Retorna o número de vértices de degeneração na malha do patch.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b2bc5-113">*pNumDegeneratePatches* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b2bc5-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2bc5-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2bc5-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b2bc5-115">Retorna o número de patches de degeneração na malha do patch.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b2bc5-116">*ppErrorsAndWarnings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b2bc5-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2bc5-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2bc5-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b2bc5-118">Retorna um ponteiro para um buffer que contém uma cadeia de caracteres de erros e avisos que explicam os problemas encontrados na malha do patch.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2bc5-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2bc5-119">Return value</span></span>

<span data-ttu-id="b2bc5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2bc5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2bc5-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2bc5-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2bc5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2bc5-123">Remarks</span></span>

<span data-ttu-id="b2bc5-124">Esse método valida a malha verificando índices inválidos.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="b2bc5-125">As informações de erro estão disponíveis na saída do depurador.</span><span class="sxs-lookup"><span data-stu-id="b2bc5-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bc5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2bc5-126">Requirements</span></span>



| <span data-ttu-id="b2bc5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2bc5-127">Requirement</span></span> | <span data-ttu-id="b2bc5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b2bc5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2bc5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2bc5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b2bc5-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2bc5-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b2bc5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2bc5-131">Library</span></span><br/> | <dl> <span data-ttu-id="b2bc5-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2bc5-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2bc5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2bc5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2bc5-134">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="b2bc5-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
