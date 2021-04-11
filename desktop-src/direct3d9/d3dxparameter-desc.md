---
description: Descreve um parâmetro usado para um objeto Effect.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Estrutura de D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172925"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="735c3-103">\_Estrutura desc de D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="735c3-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="735c3-104">Descreve um parâmetro usado para um objeto Effect.</span><span class="sxs-lookup"><span data-stu-id="735c3-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="735c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="735c3-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="735c3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="735c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="735c3-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="735c3-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-109">Nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="735c3-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-110">**Semântico**</span><span class="sxs-lookup"><span data-stu-id="735c3-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-112">Significado semântico, também chamado de uso.</span><span class="sxs-lookup"><span data-stu-id="735c3-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-113">**Classe**</span><span class="sxs-lookup"><span data-stu-id="735c3-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-114">Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-115">Classe de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="735c3-115">Parameter class.</span></span> <span data-ttu-id="735c3-116">Defina isso para um dos valores na [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="735c3-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="735c3-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="735c3-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-118">Tipo: **[ **\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-119">Tipo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="735c3-119">Parameter type.</span></span> <span data-ttu-id="735c3-120">Defina isso para um dos valores no [**\_ tipo D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="735c3-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="735c3-121">**Linhas**</span><span class="sxs-lookup"><span data-stu-id="735c3-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-123">Número de linhas na matriz.</span><span class="sxs-lookup"><span data-stu-id="735c3-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-124">**Colunas**</span><span class="sxs-lookup"><span data-stu-id="735c3-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-126">Número de colunas na matriz.</span><span class="sxs-lookup"><span data-stu-id="735c3-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-127">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="735c3-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-129">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="735c3-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-130">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="735c3-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-131">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-132">Número de anotações.</span><span class="sxs-lookup"><span data-stu-id="735c3-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-133">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="735c3-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-135">Número de membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="735c3-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="735c3-136">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="735c3-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-138">Atributos de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="735c3-138">Parameter attributes.</span></span> <span data-ttu-id="735c3-139">Consulte [constantes de efeito](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="735c3-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="735c3-140">**Bytes**</span><span class="sxs-lookup"><span data-stu-id="735c3-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="735c3-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="735c3-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="735c3-142">O tamanho do parâmetro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="735c3-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="735c3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="735c3-143">Requirements</span></span>



| <span data-ttu-id="735c3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="735c3-144">Requirement</span></span> | <span data-ttu-id="735c3-145">Valor</span><span class="sxs-lookup"><span data-stu-id="735c3-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="735c3-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="735c3-146">Header</span></span><br/> | <dl> <span data-ttu-id="735c3-147"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="735c3-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735c3-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="735c3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735c3-149">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="735c3-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
