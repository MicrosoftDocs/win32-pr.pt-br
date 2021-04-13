---
description: Uma estrutura auxiliar que contém informações de estrutura de membro.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Estrutura de D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298574"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="e85ee-103">\_Estrutura D3DXSHADER STRUCTMEMBERINFO</span><span class="sxs-lookup"><span data-stu-id="e85ee-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="e85ee-104">Uma estrutura auxiliar que contém informações de estrutura de membro.</span><span class="sxs-lookup"><span data-stu-id="e85ee-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e85ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e85ee-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="e85ee-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e85ee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e85ee-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e85ee-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="e85ee-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e85ee-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e85ee-109">Deslocamento do início desta estrutura, em bytes, para a cadeia de caracteres que contém o nome do membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="e85ee-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="e85ee-110">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="e85ee-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e85ee-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e85ee-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e85ee-112">Deslocamento do início desta estrutura, em bytes, para a cadeia de caracteres que contém as informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="e85ee-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="e85ee-113">Consulte [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).</span><span class="sxs-lookup"><span data-stu-id="e85ee-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e85ee-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e85ee-114">Requirements</span></span>



| <span data-ttu-id="e85ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e85ee-115">Requirement</span></span> | <span data-ttu-id="e85ee-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e85ee-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85ee-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e85ee-117">Header</span></span><br/> | <dl> <span data-ttu-id="e85ee-118"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e85ee-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85ee-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e85ee-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85ee-120">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="e85ee-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e85ee-121">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="e85ee-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
