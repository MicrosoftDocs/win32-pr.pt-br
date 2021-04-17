---
description: Identifica os dados de memória. Preterido.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Estrutura DXFILELOADMEMORY (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813743"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="2eba3-104">Estrutura DXFILELOADMEMORY</span><span class="sxs-lookup"><span data-stu-id="2eba3-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="2eba3-105">Identifica os dados de memória.</span><span class="sxs-lookup"><span data-stu-id="2eba3-105">Identifies memory data.</span></span> <span data-ttu-id="2eba3-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="2eba3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eba3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2eba3-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="2eba3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2eba3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2eba3-109">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="2eba3-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="2eba3-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eba3-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2eba3-111">Ponteiro para um bloco de memória a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="2eba3-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2eba3-112">**dSize**</span><span class="sxs-lookup"><span data-stu-id="2eba3-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="2eba3-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eba3-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2eba3-114">Tamanho do bloco de memória a ser carregado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2eba3-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eba3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eba3-115">Remarks</span></span>

<span data-ttu-id="2eba3-116">Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**Createenumobject**](idirectxfile--createenumobject.md) e especifica DXFILELOAD \_ FROMMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2eba3-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eba3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eba3-117">Requirements</span></span>



| <span data-ttu-id="2eba3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eba3-118">Requirement</span></span> | <span data-ttu-id="2eba3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2eba3-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2eba3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2eba3-120">Header</span></span><br/> | <dl> <span data-ttu-id="2eba3-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eba3-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eba3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eba3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eba3-123">X estruturas de arquivo</span><span class="sxs-lookup"><span data-stu-id="2eba3-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="2eba3-124">**Createenumobject**</span><span class="sxs-lookup"><span data-stu-id="2eba3-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="2eba3-125">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="2eba3-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
