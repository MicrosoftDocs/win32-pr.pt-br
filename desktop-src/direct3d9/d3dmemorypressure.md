---
description: Contém dados para o relatório de pressão de memória.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Estrutura D3DMEMORYPRESSURE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798480"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="9c967-103">Estrutura D3DMEMORYPRESSURE (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="9c967-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="9c967-104">Contém dados para o relatório de pressão de memória.</span><span class="sxs-lookup"><span data-stu-id="9c967-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c967-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c967-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="9c967-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9c967-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c967-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="9c967-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="9c967-108">Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c967-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c967-109">O número de bytes que foram removidos pelo processo durante a duração da consulta.</span><span class="sxs-lookup"><span data-stu-id="9c967-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="9c967-110">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="9c967-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="9c967-111">Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c967-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c967-112">O número total de bytes colocados em segmentos de memória não ideais, devido a espaço inadequado dentro dos segmentos de memória preferenciais.</span><span class="sxs-lookup"><span data-stu-id="9c967-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="9c967-113">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="9c967-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="9c967-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c967-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c967-115">A eficiência geral das alocações de memória que foram colocadas na memória não ideal.</span><span class="sxs-lookup"><span data-stu-id="9c967-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="9c967-116">O valor é expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="9c967-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="9c967-117">Por exemplo, o valor 95 indica que as alocações colocadas em segmentos de memória não preferenciais são 95% eficiente.</span><span class="sxs-lookup"><span data-stu-id="9c967-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="9c967-118">Esse número não deve ser considerado uma medida exata.</span><span class="sxs-lookup"><span data-stu-id="9c967-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c967-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c967-119">Requirements</span></span>



| <span data-ttu-id="9c967-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c967-120">Requirement</span></span> | <span data-ttu-id="9c967-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9c967-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c967-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c967-122">Header</span></span><br/> | <dl> <span data-ttu-id="9c967-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c967-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c967-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c967-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c967-125">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="9c967-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
