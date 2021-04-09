---
description: Contém dados para o relatório de pressão de memória.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
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
ms.openlocfilehash: 6d92cad29bda795a9589dbe0c94863bd743505bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089754"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="2d14b-103">Estrutura D3DMEMORYPRESSURE (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="2d14b-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="2d14b-104">Contém dados para o relatório de pressão de memória.</span><span class="sxs-lookup"><span data-stu-id="2d14b-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d14b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d14b-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="2d14b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2d14b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d14b-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="2d14b-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="2d14b-108">O número de bytes que foram removidos pelo processo durante a duração da consulta.</span><span class="sxs-lookup"><span data-stu-id="2d14b-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="2d14b-109">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="2d14b-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="2d14b-110">O número total de bytes colocados em segmentos de memória não ideais, devido a espaço inadequado dentro dos segmentos de memória preferenciais.</span><span class="sxs-lookup"><span data-stu-id="2d14b-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="2d14b-111">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="2d14b-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="2d14b-112">A eficiência geral das alocações de memória que foram colocadas na memória não ideal.</span><span class="sxs-lookup"><span data-stu-id="2d14b-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="2d14b-113">O valor é expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="2d14b-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="2d14b-114">Por exemplo, o valor 95 indica que as alocações colocadas em segmentos de memória não preferenciais são 95% eficiente.</span><span class="sxs-lookup"><span data-stu-id="2d14b-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="2d14b-115">Esse número não deve ser considerado uma medida exata.</span><span class="sxs-lookup"><span data-stu-id="2d14b-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d14b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d14b-116">Requirements</span></span>



| <span data-ttu-id="2d14b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d14b-117">Requirement</span></span> | <span data-ttu-id="2d14b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2d14b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d14b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d14b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d14b-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2d14b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2d14b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d14b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d14b-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="2d14b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d14b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d14b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d14b-124"><dt>D3d9types. h (incluir D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d14b-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d14b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d14b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d14b-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="2d14b-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2d14b-127">Relatório de pressão de memória</span><span class="sxs-lookup"><span data-stu-id="2d14b-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




