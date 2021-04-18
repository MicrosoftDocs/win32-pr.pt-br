---
description: Identifica os dados do recurso. Preterido.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Estrutura DXFILELOADRESOURCE (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105749903"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="d1246-104">Estrutura DXFILELOADRESOURCE</span><span class="sxs-lookup"><span data-stu-id="d1246-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="d1246-105">Identifica os dados do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1246-105">Identifies resource data.</span></span> <span data-ttu-id="d1246-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="d1246-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1246-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1246-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="d1246-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d1246-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1246-109">**hModule**</span><span class="sxs-lookup"><span data-stu-id="d1246-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="d1246-110">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1246-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1246-111">Identificador do módulo que contém o recurso a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="d1246-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="d1246-112">Se esse membro for **nulo**, o recurso deverá ser anexado ao arquivo executável que o usará.</span><span class="sxs-lookup"><span data-stu-id="d1246-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="d1246-113">**lpName**</span><span class="sxs-lookup"><span data-stu-id="d1246-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="d1246-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1246-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1246-115">Ponteiro para uma cadeia de caracteres especificando o nome do recurso a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="d1246-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="d1246-116">Por exemplo, se o recurso for uma malha, esse membro deverá especificar o nome do arquivo de malha.</span><span class="sxs-lookup"><span data-stu-id="d1246-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="d1246-117">**lpType**</span><span class="sxs-lookup"><span data-stu-id="d1246-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="d1246-118">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1246-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d1246-119">Ponteiro para uma cadeia de caracteres que especifica o tipo definido pelo usuário que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="d1246-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1246-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1246-120">Remarks</span></span>

<span data-ttu-id="d1246-121">Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**Createenumobject**](idirectxfile--createenumobject.md) e especifica DXFILELOAD \_ FROMRESOURCE.</span><span class="sxs-lookup"><span data-stu-id="d1246-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1246-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1246-122">Requirements</span></span>



| <span data-ttu-id="d1246-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1246-123">Requirement</span></span> | <span data-ttu-id="d1246-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d1246-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1246-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1246-125">Header</span></span><br/> | <dl> <span data-ttu-id="d1246-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1246-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1246-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1246-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1246-128">X estruturas de arquivo</span><span class="sxs-lookup"><span data-stu-id="d1246-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="d1246-129">**Createenumobject**</span><span class="sxs-lookup"><span data-stu-id="d1246-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="d1246-130">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="d1246-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
