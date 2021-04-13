---
description: Descreve um volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Estrutura de D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298687"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="7dee7-103">\_Estrutura desc de D3DVOLUME</span><span class="sxs-lookup"><span data-stu-id="7dee7-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="7dee7-104">Descreve um volume.</span><span class="sxs-lookup"><span data-stu-id="7dee7-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dee7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dee7-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="7dee7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7dee7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dee7-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="7dee7-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-109">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície do volume.</span><span class="sxs-lookup"><span data-stu-id="7dee7-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7dee7-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-112">Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como um volume.</span><span class="sxs-lookup"><span data-stu-id="7dee7-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-113">**Usage**</span><span class="sxs-lookup"><span data-stu-id="7dee7-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-115">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="7dee7-115">Currently not used.</span></span> <span data-ttu-id="7dee7-116">Sempre retornado como 0.</span><span class="sxs-lookup"><span data-stu-id="7dee7-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="7dee7-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-118">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-119">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para esse volume.</span><span class="sxs-lookup"><span data-stu-id="7dee7-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-120">**Largura**</span><span class="sxs-lookup"><span data-stu-id="7dee7-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-122">Largura do volume, em pixels.</span><span class="sxs-lookup"><span data-stu-id="7dee7-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-123">**Altura**</span><span class="sxs-lookup"><span data-stu-id="7dee7-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-125">Altura do volume, em pixels.</span><span class="sxs-lookup"><span data-stu-id="7dee7-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-126">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="7dee7-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dee7-128">Profundidade do volume, em pixels.</span><span class="sxs-lookup"><span data-stu-id="7dee7-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dee7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dee7-129">Requirements</span></span>



| <span data-ttu-id="7dee7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dee7-130">Requirement</span></span> | <span data-ttu-id="7dee7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7dee7-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dee7-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dee7-132">Header</span></span><br/> | <dl> <span data-ttu-id="7dee7-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dee7-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dee7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dee7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dee7-135">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="7dee7-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="7dee7-136">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="7dee7-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="7dee7-137">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="7dee7-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
