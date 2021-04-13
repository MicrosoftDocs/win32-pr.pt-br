---
description: Estrutura de dados de malha.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: Estrutura D3DXMESHDATA (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298484"
---
# <a name="d3dxmeshdata-structure"></a><span data-ttu-id="a897b-103">Estrutura D3DXMESHDATA</span><span class="sxs-lookup"><span data-stu-id="a897b-103">D3DXMESHDATA structure</span></span>

<span data-ttu-id="a897b-104">Estrutura de dados de malha.</span><span class="sxs-lookup"><span data-stu-id="a897b-104">Mesh data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a897b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a897b-105">Syntax</span></span>


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a><span data-ttu-id="a897b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a897b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a897b-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a897b-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="a897b-108">Tipo: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span><span class="sxs-lookup"><span data-stu-id="a897b-108">Type: **[**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a897b-109">Define o tipo de dados de malha.</span><span class="sxs-lookup"><span data-stu-id="a897b-109">Defines the mesh data type.</span></span> <span data-ttu-id="a897b-110">Consulte [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span><span class="sxs-lookup"><span data-stu-id="a897b-110">See [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a897b-111">**pMesh**</span><span class="sxs-lookup"><span data-stu-id="a897b-111">**pMesh**</span></span>
</dt> <dd>

<span data-ttu-id="a897b-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a897b-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a897b-113">Ponteiro para uma malha.</span><span class="sxs-lookup"><span data-stu-id="a897b-113">Pointer to a mesh.</span></span> <span data-ttu-id="a897b-114">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="a897b-114">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="a897b-115">**pPatchMesh**</span><span class="sxs-lookup"><span data-stu-id="a897b-115">**pPatchMesh**</span></span>
</dt> <dd>

<span data-ttu-id="a897b-116">Tipo: **LPD3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="a897b-116">Type: **LPD3DXPATCHMESH**</span></span>

</dd> <dd>

<span data-ttu-id="a897b-117">Ponteiro para uma malha de patch.</span><span class="sxs-lookup"><span data-stu-id="a897b-117">Pointer to a patch mesh.</span></span> <span data-ttu-id="a897b-118">Consulte [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="a897b-118">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a897b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a897b-119">Requirements</span></span>



| <span data-ttu-id="a897b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a897b-120">Requirement</span></span> | <span data-ttu-id="a897b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a897b-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a897b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a897b-122">Header</span></span><br/> | <dl> <span data-ttu-id="a897b-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a897b-123"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a897b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a897b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a897b-125">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="a897b-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a897b-126">**D3DXMESHCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="a897b-126">**D3DXMESHCONTAINER**</span></span>](d3dxmeshcontainer.md)
</dt> </dl>

 

 
