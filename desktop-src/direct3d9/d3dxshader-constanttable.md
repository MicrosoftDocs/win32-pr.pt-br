---
description: Estrutura auxiliar para gerenciar uma tabela de constante de sombreador. Isso também pode ser feito usando o ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Estrutura de D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788741"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="64fe8-104">\_Estrutura de constante D3DXSHADER</span><span class="sxs-lookup"><span data-stu-id="64fe8-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="64fe8-105">Estrutura auxiliar para gerenciar uma tabela de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="64fe8-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="64fe8-106">Isso também pode ser feito usando o [**ID3DXConstantTable**](id3dxconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="64fe8-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64fe8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64fe8-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="64fe8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="64fe8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="64fe8-109">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="64fe8-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-111">Tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="64fe8-111">Size of the structure.</span></span> <span data-ttu-id="64fe8-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="64fe8-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="64fe8-113">**Criador**</span><span class="sxs-lookup"><span data-stu-id="64fe8-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-115">Offset do início desta estrutura, em bytes, para a cadeia de caracteres que contém o nome do criador.</span><span class="sxs-lookup"><span data-stu-id="64fe8-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="64fe8-116">**Versão**</span><span class="sxs-lookup"><span data-stu-id="64fe8-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-118">Versão do sombreador.</span><span class="sxs-lookup"><span data-stu-id="64fe8-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="64fe8-119">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="64fe8-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-121">Número de constantes.</span><span class="sxs-lookup"><span data-stu-id="64fe8-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="64fe8-122">**ConstantInfo**</span><span class="sxs-lookup"><span data-stu-id="64fe8-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-124">Matriz de informações constantes, \_ constantes D3DXSHADER CONSTANTINFO \[  \] .</span><span class="sxs-lookup"><span data-stu-id="64fe8-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="64fe8-125">Consulte [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).</span><span class="sxs-lookup"><span data-stu-id="64fe8-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="64fe8-126">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="64fe8-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-128">Os sinalizadores de [sinalizadores D3DXSHADER](d3dxshader-flags.md) usados para compilar o sombreador.</span><span class="sxs-lookup"><span data-stu-id="64fe8-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="64fe8-129">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="64fe8-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64fe8-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="64fe8-131">Deslocamento na cadeia de caracteres que contém o destino.</span><span class="sxs-lookup"><span data-stu-id="64fe8-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64fe8-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="64fe8-132">Remarks</span></span>

<span data-ttu-id="64fe8-133">As informações constantes do sombreador estão incluídas em uma tabela de comentários delimitada por tabulação.</span><span class="sxs-lookup"><span data-stu-id="64fe8-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="64fe8-134">Todos os deslocamentos são medidos em bytes desde o início da estrutura.</span><span class="sxs-lookup"><span data-stu-id="64fe8-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="64fe8-135">As entradas na tabela de constantes são classificadas por criador em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="64fe8-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="64fe8-136">Uma tabela de constantes de sombreador pode ser gerenciada com as interfaces [**ID3DXConstantTable**](id3dxconstanttable.md) .</span><span class="sxs-lookup"><span data-stu-id="64fe8-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="64fe8-137">Como alternativa, você pode gerenciar a tabela constante com **a \_ constante D3DXSHADER**.</span><span class="sxs-lookup"><span data-stu-id="64fe8-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="64fe8-138">Esse membro de tamanho geralmente é inicializado usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="64fe8-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="64fe8-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64fe8-139">Requirements</span></span>



| <span data-ttu-id="64fe8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="64fe8-140">Requirement</span></span> | <span data-ttu-id="64fe8-141">Valor</span><span class="sxs-lookup"><span data-stu-id="64fe8-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64fe8-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64fe8-142">Header</span></span><br/> | <dl> <span data-ttu-id="64fe8-143"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="64fe8-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64fe8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="64fe8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64fe8-145">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="64fe8-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="64fe8-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="64fe8-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
