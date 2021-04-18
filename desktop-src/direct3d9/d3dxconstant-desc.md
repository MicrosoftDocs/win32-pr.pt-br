---
description: Uma descrição de uma constante em uma tabela constante.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: Estrutura de D3DXCONSTANT_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790323"
---
# <a name="d3dxconstant_desc-structure"></a><span data-ttu-id="61b7d-103">\_Estrutura desc de D3DXCONSTANT</span><span class="sxs-lookup"><span data-stu-id="61b7d-103">D3DXCONSTANT\_DESC structure</span></span>

<span data-ttu-id="61b7d-104">Uma descrição de uma constante em uma tabela constante.</span><span class="sxs-lookup"><span data-stu-id="61b7d-104">A description of a constant in a constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61b7d-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a><span data-ttu-id="61b7d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="61b7d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="61b7d-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="61b7d-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-109">Nome da constante.</span><span class="sxs-lookup"><span data-stu-id="61b7d-109">Name of the constant.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-110">**Registroset**</span><span class="sxs-lookup"><span data-stu-id="61b7d-110">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-111">Tipo: **[ **D3DXREGISTER \_ definido**](./d3dxregister-set.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-111">Type: **[**D3DXREGISTER\_SET**](./d3dxregister-set.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-112">Tipo de dados Constant.</span><span class="sxs-lookup"><span data-stu-id="61b7d-112">Constant data type.</span></span> <span data-ttu-id="61b7d-113">Consulte [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="61b7d-113">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-114">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="61b7d-114">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-116">Índice de base zero da constante na tabela.</span><span class="sxs-lookup"><span data-stu-id="61b7d-116">Zero-based index of the constant in the table.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-117">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="61b7d-117">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-119">Número de registros que contêm dados.</span><span class="sxs-lookup"><span data-stu-id="61b7d-119">Number of registers that contain data.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-120">**Classe**</span><span class="sxs-lookup"><span data-stu-id="61b7d-120">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-121">Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-121">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-122">Classe de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61b7d-122">Parameter class.</span></span> <span data-ttu-id="61b7d-123">Consulte [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="61b7d-123">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61b7d-124">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-125">Tipo: **[ **\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-125">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-126">Tipo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61b7d-126">Parameter type.</span></span> <span data-ttu-id="61b7d-127">Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="61b7d-127">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-128">**Linhas**</span><span class="sxs-lookup"><span data-stu-id="61b7d-128">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-130">Número de linhas.</span><span class="sxs-lookup"><span data-stu-id="61b7d-130">Number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-131">**Colunas**</span><span class="sxs-lookup"><span data-stu-id="61b7d-131">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-133">Número de colunas.</span><span class="sxs-lookup"><span data-stu-id="61b7d-133">Number of columns.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-134">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="61b7d-134">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-136">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="61b7d-136">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-137">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="61b7d-137">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-138">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-139">Número de subparâmetros de membro de estrutura.</span><span class="sxs-lookup"><span data-stu-id="61b7d-139">Number of structure member sub-parameters.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-140">**Bytes**</span><span class="sxs-lookup"><span data-stu-id="61b7d-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-142">Tamanho dos dados em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="61b7d-142">Data size in number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-143">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="61b7d-143">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="61b7d-144">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-144">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61b7d-145">Ponteiro para o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="61b7d-145">Pointer to the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61b7d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b7d-146">Requirements</span></span>



| <span data-ttu-id="61b7d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b7d-147">Requirement</span></span> | <span data-ttu-id="61b7d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="61b7d-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b7d-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61b7d-149">Header</span></span><br/> | <dl> <span data-ttu-id="61b7d-150"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b7d-150"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b7d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="61b7d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b7d-152">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="61b7d-152">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="61b7d-153">**D3DXCONSTANTTABLE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="61b7d-153">**D3DXCONSTANTTABLE\_DESC**</span></span>](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
