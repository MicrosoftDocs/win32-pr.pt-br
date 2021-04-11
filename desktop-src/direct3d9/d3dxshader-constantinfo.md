---
description: '\_Estrutura D3DXSHADER CONSTANTINFO'
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Estrutura de D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172984"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="586b2-103">\_Estrutura D3DXSHADER CONSTANTINFO</span><span class="sxs-lookup"><span data-stu-id="586b2-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="586b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="586b2-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="586b2-105">Membros</span><span class="sxs-lookup"><span data-stu-id="586b2-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="586b2-106">**Nome**</span><span class="sxs-lookup"><span data-stu-id="586b2-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-107">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-108">Deslocamento do início desta estrutura, em bytes, para a cadeia de caracteres que contém as informações de constante.</span><span class="sxs-lookup"><span data-stu-id="586b2-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="586b2-109">**Registroset**</span><span class="sxs-lookup"><span data-stu-id="586b2-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-110">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-111">Conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="586b2-111">Register set.</span></span> <span data-ttu-id="586b2-112">Consulte [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="586b2-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="586b2-113">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="586b2-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-114">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-115">O índice de registro.</span><span class="sxs-lookup"><span data-stu-id="586b2-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="586b2-116">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="586b2-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-117">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-118">Número de registros.</span><span class="sxs-lookup"><span data-stu-id="586b2-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="586b2-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="586b2-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-120">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="586b2-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="586b2-122">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="586b2-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-124">Offset do início desta estrutura, em bytes, para a cadeia de caracteres que contém as informações do [**\_ TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="586b2-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="586b2-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="586b2-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="586b2-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="586b2-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="586b2-127">Deslocamento do início desta estrutura, em bytes, para a cadeia de caracteres que contém o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="586b2-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="586b2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="586b2-128">Requirements</span></span>



| <span data-ttu-id="586b2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="586b2-129">Requirement</span></span> | <span data-ttu-id="586b2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="586b2-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="586b2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="586b2-131">Header</span></span><br/> | <dl> <span data-ttu-id="586b2-132"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="586b2-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586b2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="586b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586b2-134">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="586b2-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
