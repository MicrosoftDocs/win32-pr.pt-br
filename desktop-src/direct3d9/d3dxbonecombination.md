---
description: Descreve um subconjunto da malha que tem a mesma combinação de atributo e Bone.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Estrutura D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012113"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="81c7f-103">Estrutura D3DXBONECOMBINATION</span><span class="sxs-lookup"><span data-stu-id="81c7f-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="81c7f-104">Descreve um subconjunto da malha que tem a mesma combinação de atributo e Bone.</span><span class="sxs-lookup"><span data-stu-id="81c7f-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81c7f-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="81c7f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="81c7f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81c7f-107">**Atribid**</span><span class="sxs-lookup"><span data-stu-id="81c7f-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="81c7f-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81c7f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81c7f-109">Identificador de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="81c7f-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="81c7f-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="81c7f-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="81c7f-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81c7f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81c7f-112">Iniciando face.</span><span class="sxs-lookup"><span data-stu-id="81c7f-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="81c7f-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="81c7f-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="81c7f-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81c7f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81c7f-115">Contagem de face.</span><span class="sxs-lookup"><span data-stu-id="81c7f-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="81c7f-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="81c7f-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="81c7f-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81c7f-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81c7f-118">Iniciando vértice.</span><span class="sxs-lookup"><span data-stu-id="81c7f-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="81c7f-119">**Contagemdevértice**</span><span class="sxs-lookup"><span data-stu-id="81c7f-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="81c7f-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81c7f-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81c7f-121">Contagem de vértices.</span><span class="sxs-lookup"><span data-stu-id="81c7f-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="81c7f-122">**Boneid**</span><span class="sxs-lookup"><span data-stu-id="81c7f-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="81c7f-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="81c7f-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="81c7f-124">Ponteiro para uma matriz de valores que identifica cada um dos Bones que podem ser desenhados em uma única chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="81c7f-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="81c7f-125">Observe que a matriz pode ser de comprimento variável para acomodar combinações Bone de comprimento variável de [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span><span class="sxs-lookup"><span data-stu-id="81c7f-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="81c7f-126">O tamanho da matriz varia de acordo com o tipo de malha gerada.</span><span class="sxs-lookup"><span data-stu-id="81c7f-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="81c7f-127">Um tamanho de matriz de malha não indexada é igual ao número de pesos por vértice (pMaxVertexInfl em [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="81c7f-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="81c7f-128">Um tamanho de matriz de malha indexada é igual ao número de entradas da paleta de matriz Bone (paletteSize em [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="81c7f-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81c7f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="81c7f-129">Remarks</span></span>

<span data-ttu-id="81c7f-130">O subconjunto da malha descrito por **D3DXBONECOMBINATION** pode ser renderizado em uma única chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="81c7f-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="81c7f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81c7f-131">Requirements</span></span>



| <span data-ttu-id="81c7f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="81c7f-132">Requirement</span></span> | <span data-ttu-id="81c7f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="81c7f-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81c7f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81c7f-134">Header</span></span><br/> | <dl> <span data-ttu-id="81c7f-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="81c7f-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81c7f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="81c7f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c7f-137">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="81c7f-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
