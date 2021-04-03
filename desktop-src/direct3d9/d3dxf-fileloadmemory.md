---
description: Identifica os dados de memória.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Estrutura de D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930596"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="07c02-103">\_Estrutura D3DXF FILELOADMEMORY</span><span class="sxs-lookup"><span data-stu-id="07c02-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="07c02-104">Identifica os dados de memória.</span><span class="sxs-lookup"><span data-stu-id="07c02-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07c02-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="07c02-106">Membros</span><span class="sxs-lookup"><span data-stu-id="07c02-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07c02-107">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="07c02-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="07c02-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c02-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07c02-109">Ponteiro para um bloco de memória a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="07c02-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="07c02-110">**dSize**</span><span class="sxs-lookup"><span data-stu-id="07c02-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="07c02-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c02-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07c02-112">Tamanho do bloco de memória a ser carregado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="07c02-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07c02-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="07c02-113">Remarks</span></span>

<span data-ttu-id="07c02-114">Essa estrutura identifica os dados a serem carregados da memória quando um aplicativo usa o método [**Createenumobject**](id3dxfile--createenumobject.md) e especifica o \_ sinalizador FROMMEMORY do D3DXF fileload \_ .</span><span class="sxs-lookup"><span data-stu-id="07c02-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c02-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c02-115">Requirements</span></span>



| <span data-ttu-id="07c02-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c02-116">Requirement</span></span> | <span data-ttu-id="07c02-117">Valor</span><span class="sxs-lookup"><span data-stu-id="07c02-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07c02-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07c02-118">Header</span></span><br/> | <dl> <span data-ttu-id="07c02-119"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c02-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c02-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="07c02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c02-121">Estruturas de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="07c02-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
