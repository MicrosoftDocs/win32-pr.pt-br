---
description: Estatísticas de uso de recursos.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Estrutura de D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663978"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="099b0-103">\_Estrutura de RESOURCEMANAGER D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="099b0-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="099b0-104">Estatísticas de uso de recursos.</span><span class="sxs-lookup"><span data-stu-id="099b0-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="099b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="099b0-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="099b0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="099b0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="099b0-107">**Estatísticas**</span><span class="sxs-lookup"><span data-stu-id="099b0-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="099b0-108">Tipo: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="099b0-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="099b0-109">Matriz de elementos de estatísticas de recursos.</span><span class="sxs-lookup"><span data-stu-id="099b0-109">Array of resource statistics elements.</span></span> <span data-ttu-id="099b0-110">Consulte [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="099b0-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="099b0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="099b0-111">Remarks</span></span>

<span data-ttu-id="099b0-112">D3DRTYPECOUNT refere-se ao número de enumerações em [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="099b0-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="099b0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="099b0-113">Requirements</span></span>



| <span data-ttu-id="099b0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="099b0-114">Requirement</span></span> | <span data-ttu-id="099b0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="099b0-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="099b0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="099b0-116">Header</span></span><br/> | <dl> <span data-ttu-id="099b0-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="099b0-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099b0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="099b0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099b0-119">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="099b0-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
