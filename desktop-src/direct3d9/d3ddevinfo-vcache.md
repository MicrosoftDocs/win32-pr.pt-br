---
description: Dicas de otimização do cache de vértice.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Estrutura de D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769372"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="981e1-103">\_Estrutura D3DDEVINFO VCACHE</span><span class="sxs-lookup"><span data-stu-id="981e1-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="981e1-104">Dicas de otimização do cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="981e1-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="981e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="981e1-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="981e1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="981e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="981e1-107">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="981e1-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="981e1-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="981e1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="981e1-109">Padrão de bits.</span><span class="sxs-lookup"><span data-stu-id="981e1-109">Bit pattern.</span></span> <span data-ttu-id="981e1-110">O valor de retorno deve ser o FOURCC (' C', ' A ', ' C', ' H ').</span><span class="sxs-lookup"><span data-stu-id="981e1-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="981e1-111">**OptMethod**</span><span class="sxs-lookup"><span data-stu-id="981e1-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="981e1-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="981e1-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="981e1-113">Método de otimizações.</span><span class="sxs-lookup"><span data-stu-id="981e1-113">Optimizations method.</span></span> <span data-ttu-id="981e1-114">Use 0 para obter as faixas mais longas.</span><span class="sxs-lookup"><span data-stu-id="981e1-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="981e1-115">Use 1 para otimizar o uso do cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="981e1-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="981e1-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="981e1-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="981e1-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="981e1-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="981e1-118">Tamanho do cache usado como um destino para otimização.</span><span class="sxs-lookup"><span data-stu-id="981e1-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="981e1-119">Isso será necessário somente se OptMethod for 1.</span><span class="sxs-lookup"><span data-stu-id="981e1-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="981e1-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="981e1-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="981e1-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="981e1-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="981e1-122">Usado por métodos de otimização internos para determinar quando reiniciar as faixas.</span><span class="sxs-lookup"><span data-stu-id="981e1-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="981e1-123">Isso não pode ser definido ou modificado por um usuário.</span><span class="sxs-lookup"><span data-stu-id="981e1-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="981e1-124">Isso será necessário somente se OptMethod for 1.</span><span class="sxs-lookup"><span data-stu-id="981e1-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="981e1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="981e1-125">Requirements</span></span>



| <span data-ttu-id="981e1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="981e1-126">Requirement</span></span> | <span data-ttu-id="981e1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="981e1-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="981e1-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="981e1-128">Header</span></span><br/> | <dl> <span data-ttu-id="981e1-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="981e1-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="981e1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="981e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981e1-131">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="981e1-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="981e1-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="981e1-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
