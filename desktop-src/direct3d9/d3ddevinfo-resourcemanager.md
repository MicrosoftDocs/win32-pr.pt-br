---
description: Estatísticas de uso de recursos.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_RESOURCEMANAGER (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b0a9fc461564280e4e36dde6bf73e68a78cf1609
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129975"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="c0041-103">Estrutura D3DDEVINFO \_ RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="c0041-103">D3DDEVINFO\_RESOURCEMANAGER structure</span></span>

<span data-ttu-id="c0041-104">Estatísticas de uso de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0041-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0041-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0041-105">Syntax</span></span>


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a><span data-ttu-id="c0041-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c0041-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0041-107">**Estatísticas**</span><span class="sxs-lookup"><span data-stu-id="c0041-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="c0041-108">Tipo: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="c0041-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0041-109">Matriz de elementos de estatísticas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c0041-109">Array of resource statistics elements.</span></span> <span data-ttu-id="c0041-110">Consulte [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="c0041-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0041-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0041-111">Remarks</span></span>

<span data-ttu-id="c0041-112">D3DRTYPECOUNT refere-se ao número de enumerações em [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="c0041-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0041-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0041-113">Requirements</span></span>



| <span data-ttu-id="c0041-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0041-114">Requirement</span></span> | <span data-ttu-id="c0041-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c0041-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0041-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0041-116">Header</span></span><br/> | <dl> <span data-ttu-id="c0041-117"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="c0041-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0041-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0041-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0041-119">Estruturas Direct3D</span><span class="sxs-lookup"><span data-stu-id="c0041-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
