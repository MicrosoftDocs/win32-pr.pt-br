---
description: Função D3DXCreateSkinInfo – cria um objeto de malha de capa vazio usando um Declarador.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Função D3DXCreateSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da582d791b27d30c78583972e6f598af8af3eb9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102734"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="ea0f9-103">Função D3DXCreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="ea0f9-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="ea0f9-104">Cria um objeto de malha de capa vazio usando um Declarador.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea0f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea0f9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ea0f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea0f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea0f9-107">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea0f9-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0f9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea0f9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea0f9-109">Número de vértices para a malha de capa.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ea0f9-110">*pDeclaration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea0f9-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0f9-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea0f9-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="ea0f9-112">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice para a malha retornada.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ea0f9-113">*NumBones* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea0f9-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0f9-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea0f9-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea0f9-115">Número de Bones para a malha de capa.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ea0f9-116">*ppSkinInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ea0f9-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0f9-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea0f9-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="ea0f9-118">Endereço de um ponteiro para uma interface [**ID3DXSkinInfo**](id3dxskininfo.md) , que representa o objeto de malha de capa criado.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea0f9-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ea0f9-119">Return value</span></span>

<span data-ttu-id="ea0f9-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea0f9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea0f9-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea0f9-122">Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0f9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea0f9-123">Remarks</span></span>

<span data-ttu-id="ea0f9-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) para popular o objeto de malha de capa vazio retornado por esse método.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0f9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea0f9-125">Requirements</span></span>



| <span data-ttu-id="ea0f9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea0f9-126">Requirement</span></span> | <span data-ttu-id="ea0f9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0f9-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0f9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea0f9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ea0f9-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f9-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ea0f9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea0f9-130">Library</span></span><br/> | <dl> <span data-ttu-id="ea0f9-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f9-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea0f9-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ea0f9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0f9-133">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="ea0f9-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ea0f9-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="ea0f9-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
