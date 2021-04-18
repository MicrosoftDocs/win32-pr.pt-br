---
description: Cria uma malha de N-patch de uma malha de triângulo.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: Função D3DXCreateNPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761198"
---
# <a name="d3dxcreatenpatchmesh-function"></a><span data-ttu-id="c322d-103">Função D3DXCreateNPatchMesh</span><span class="sxs-lookup"><span data-stu-id="c322d-103">D3DXCreateNPatchMesh function</span></span>

<span data-ttu-id="c322d-104">Cria uma malha de N-patch de uma malha de triângulo.</span><span class="sxs-lookup"><span data-stu-id="c322d-104">Creates an N-patch mesh from a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c322d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c322d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="c322d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c322d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c322d-107">*pMeshSysMem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c322d-107">*pMeshSysMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c322d-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c322d-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c322d-109">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) que representa o objeto de malha de triângulo.</span><span class="sxs-lookup"><span data-stu-id="c322d-109">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represents the triangle mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="c322d-110">*pPatchMesh* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c322d-110">*pPatchMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c322d-111">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c322d-111">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="c322d-112">Endereço de um ponteiro para uma interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa o objeto de malha de patch criado.</span><span class="sxs-lookup"><span data-stu-id="c322d-112">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the created patch mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c322d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c322d-113">Return value</span></span>

<span data-ttu-id="c322d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c322d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c322d-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c322d-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c322d-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c322d-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c322d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c322d-117">Requirements</span></span>



| <span data-ttu-id="c322d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c322d-118">Requirement</span></span> | <span data-ttu-id="c322d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c322d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c322d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c322d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c322d-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c322d-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c322d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c322d-122">Library</span></span><br/> | <dl> <span data-ttu-id="c322d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c322d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c322d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c322d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c322d-125">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="c322d-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




