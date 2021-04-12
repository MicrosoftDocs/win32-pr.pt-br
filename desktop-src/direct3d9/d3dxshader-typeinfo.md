---
description: Uma estrutura auxiliar que contém informações de tipo de membro.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Estrutura de D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298592"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="005ef-103">\_Estrutura de TYPEINFO D3DXSHADER</span><span class="sxs-lookup"><span data-stu-id="005ef-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="005ef-104">Uma estrutura auxiliar que contém informações de tipo de membro.</span><span class="sxs-lookup"><span data-stu-id="005ef-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="005ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="005ef-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="005ef-106">Membros</span><span class="sxs-lookup"><span data-stu-id="005ef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="005ef-107">**Classe**</span><span class="sxs-lookup"><span data-stu-id="005ef-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-109">Tipo de objeto Shader.</span><span class="sxs-lookup"><span data-stu-id="005ef-109">Shader object type.</span></span> <span data-ttu-id="005ef-110">Consulte [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="005ef-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="005ef-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="005ef-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-112">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-113">Tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="005ef-113">Data type.</span></span> <span data-ttu-id="005ef-114">Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="005ef-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="005ef-115">**Linhas**</span><span class="sxs-lookup"><span data-stu-id="005ef-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-116">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-117">Número de linhas de matriz (matrizes).</span><span class="sxs-lookup"><span data-stu-id="005ef-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="005ef-118">**Colunas**</span><span class="sxs-lookup"><span data-stu-id="005ef-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-119">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-120">Número de colunas (vetores e matrizes).</span><span class="sxs-lookup"><span data-stu-id="005ef-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="005ef-121">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="005ef-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-122">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-123">Dimensão da matriz.</span><span class="sxs-lookup"><span data-stu-id="005ef-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="005ef-124">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="005ef-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-125">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-126">Número de membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="005ef-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="005ef-127">**StructMemberInfo**</span><span class="sxs-lookup"><span data-stu-id="005ef-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="005ef-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="005ef-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="005ef-129">Matriz de informações de membro de estrutura, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] .</span><span class="sxs-lookup"><span data-stu-id="005ef-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="005ef-130">Consulte [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="005ef-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="005ef-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="005ef-131">Remarks</span></span>

<span data-ttu-id="005ef-132">As informações de tipo fazem parte de [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="005ef-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="005ef-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="005ef-133">Requirements</span></span>



| <span data-ttu-id="005ef-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="005ef-134">Requirement</span></span> | <span data-ttu-id="005ef-135">Valor</span><span class="sxs-lookup"><span data-stu-id="005ef-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="005ef-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="005ef-136">Header</span></span><br/> | <dl> <span data-ttu-id="005ef-137"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="005ef-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005ef-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="005ef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005ef-139">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="005ef-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="005ef-140">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="005ef-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
