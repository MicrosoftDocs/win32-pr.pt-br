---
description: Identifica os dados do recurso.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Estrutura de D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781217"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="65c53-103">\_Estrutura D3DXF FILELOADRESOURCE</span><span class="sxs-lookup"><span data-stu-id="65c53-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="65c53-104">Identifica os dados do recurso.</span><span class="sxs-lookup"><span data-stu-id="65c53-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65c53-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="65c53-106">Membros</span><span class="sxs-lookup"><span data-stu-id="65c53-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65c53-107">**hModule**</span><span class="sxs-lookup"><span data-stu-id="65c53-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="65c53-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65c53-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65c53-109">Identificador do módulo que contém o recurso a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="65c53-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="65c53-110">Se esse membro for **nulo**, o recurso deverá ser anexado ao arquivo executável que o usará.</span><span class="sxs-lookup"><span data-stu-id="65c53-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="65c53-111">**lpName**</span><span class="sxs-lookup"><span data-stu-id="65c53-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="65c53-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65c53-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65c53-113">Ponteiro para uma cadeia de caracteres especificando o nome do recurso a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="65c53-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="65c53-114">Por exemplo, se o recurso for uma malha, esse membro deverá especificar o nome do arquivo de malha.</span><span class="sxs-lookup"><span data-stu-id="65c53-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="65c53-115">**lpType**</span><span class="sxs-lookup"><span data-stu-id="65c53-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="65c53-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65c53-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65c53-117">Ponteiro para uma cadeia de caracteres que especifica o tipo definido pelo usuário que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="65c53-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65c53-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="65c53-118">Remarks</span></span>

<span data-ttu-id="65c53-119">Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**Createenumobject**](id3dxfile--createenumobject.md) e especifica o [sinalizador \_ \_ FROMRESOURCE fileload D3DXF](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="65c53-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c53-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65c53-120">Requirements</span></span>



| <span data-ttu-id="65c53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="65c53-121">Requirement</span></span> | <span data-ttu-id="65c53-122">Valor</span><span class="sxs-lookup"><span data-stu-id="65c53-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65c53-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65c53-123">Header</span></span><br/> | <dl> <span data-ttu-id="65c53-124"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c53-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c53-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="65c53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c53-126">Estruturas de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="65c53-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
