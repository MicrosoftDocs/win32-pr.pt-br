---
description: Cria um objeto de malha de capa vazio usando um código de formato de vértice flexível (FVF).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: Função D3DXCreateSkinInfoFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761617"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="d0e68-103">Função D3DXCreateSkinInfoFVF</span><span class="sxs-lookup"><span data-stu-id="d0e68-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="d0e68-104">Cria um objeto de malha de capa vazio usando um código de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="d0e68-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0e68-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d0e68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0e68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e68-107">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0e68-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e68-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0e68-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0e68-109">Número de vértices para a malha de capa.</span><span class="sxs-lookup"><span data-stu-id="d0e68-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d0e68-110">*FVF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0e68-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e68-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0e68-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0e68-112">Combinação de [D3DFVF](d3dfvf.md) que descreve o formato de vértice para a malha de capa retornada.</span><span class="sxs-lookup"><span data-stu-id="d0e68-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d0e68-113">*NumBones* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0e68-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e68-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0e68-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0e68-115">Número de Bones para a malha de capa.</span><span class="sxs-lookup"><span data-stu-id="d0e68-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d0e68-116">*ppSkinInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d0e68-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e68-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0e68-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="d0e68-118">Endereço de um ponteiro para uma interface [**ID3DXSkinInfo**](id3dxskininfo.md) , que representa o objeto de informações de capa criado.</span><span class="sxs-lookup"><span data-stu-id="d0e68-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e68-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0e68-119">Return value</span></span>

<span data-ttu-id="d0e68-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0e68-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0e68-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0e68-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0e68-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d0e68-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e68-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0e68-123">Remarks</span></span>

<span data-ttu-id="d0e68-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) para popular o objeto de malha de capa vazio retornado por esse método.</span><span class="sxs-lookup"><span data-stu-id="d0e68-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e68-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e68-125">Requirements</span></span>



| <span data-ttu-id="d0e68-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e68-126">Requirement</span></span> | <span data-ttu-id="d0e68-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d0e68-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e68-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0e68-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d0e68-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e68-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d0e68-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0e68-130">Library</span></span><br/> | <dl> <span data-ttu-id="d0e68-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0e68-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0e68-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0e68-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e68-133">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="d0e68-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d0e68-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="d0e68-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
