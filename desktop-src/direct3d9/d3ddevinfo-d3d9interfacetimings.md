---
description: Porcentagem de tempo de processamento de dados no driver. Essas estatísticas podem ajudar a identificar casos em que o driver está aguardando outros recursos.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Estrutura de D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751108"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="c408b-104">\_Estrutura D3DDEVINFO D3D9INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="c408b-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="c408b-105">Porcentagem de tempo de processamento de dados no driver.</span><span class="sxs-lookup"><span data-stu-id="c408b-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="c408b-106">Essas estatísticas podem ajudar a identificar casos em que o driver está aguardando outros recursos.</span><span class="sxs-lookup"><span data-stu-id="c408b-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c408b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c408b-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="c408b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c408b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c408b-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c408b-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c408b-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c408b-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c408b-111">Porcentagem de tempo que o driver gastou aguardando a GPU terminar usando um recurso bloqueado (e [D3DLOCK \_ DONOTWAIT](d3dlock.md) não foi especificado).</span><span class="sxs-lookup"><span data-stu-id="c408b-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="c408b-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c408b-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c408b-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c408b-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c408b-114">Porcentagem de tempo que o driver gastou aguardando a GPU concluir o processamento de alguns comandos antes que o driver pudesse enviar mais.</span><span class="sxs-lookup"><span data-stu-id="c408b-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="c408b-115">Isso indica que o driver ficou sem espaço para enviar comandos para a GPU.</span><span class="sxs-lookup"><span data-stu-id="c408b-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="c408b-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c408b-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c408b-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c408b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c408b-118">Porcentagem de tempo que o driver gastou aguardando a latência da GPU reduzir para menos de três quadros de renderização.</span><span class="sxs-lookup"><span data-stu-id="c408b-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="c408b-119">Se um aplicativo for limitado à GPU, o driver deverá paralisar a CPU até que a GPU fique dentro de três quadros.</span><span class="sxs-lookup"><span data-stu-id="c408b-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="c408b-120">Isso impede que um aplicativo enfileirar muitos segundos de processamento de chamadas, o que pode aumentar consideravelmente a latência entre quando o usuário insere novos dados e quando o usuário vê os resultados dessa entrada.</span><span class="sxs-lookup"><span data-stu-id="c408b-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="c408b-121">Em geral, o driver pode acompanhar o número de vezes que o [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) é chamado para impedir o enfileiramento de mais de três quadros de trabalho de renderização.</span><span class="sxs-lookup"><span data-stu-id="c408b-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="c408b-122">**WaitingForGPUExclusiveResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c408b-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c408b-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c408b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c408b-124">Porcentagem de tempo que o driver gastou aguardando um recurso que não pode ser canalizado (que é operado em paralelo).</span><span class="sxs-lookup"><span data-stu-id="c408b-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="c408b-125">Um aplicativo pode querer evitar o uso de um recurso não-pipeline por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c408b-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="c408b-126">**WaitingForGPUOtherTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c408b-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c408b-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c408b-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c408b-128">Porcentagem de tempo que o driver gastou esperando por outro processamento de GPU.</span><span class="sxs-lookup"><span data-stu-id="c408b-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c408b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="c408b-129">Remarks</span></span>

<span data-ttu-id="c408b-130">Essas métricas ajudam a identificar quando um driver está aguardando e o que está aguardando.</span><span class="sxs-lookup"><span data-stu-id="c408b-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="c408b-131">Porcentagens altas não são necessariamente um problema.</span><span class="sxs-lookup"><span data-stu-id="c408b-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="c408b-132">Essas métricas globais do sistema podem ou não ser implementadas.</span><span class="sxs-lookup"><span data-stu-id="c408b-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="c408b-133">Dependendo do hardware específico, essas métricas podem não dar suporte a várias consultas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="c408b-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c408b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c408b-134">Requirements</span></span>



| <span data-ttu-id="c408b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c408b-135">Requirement</span></span> | <span data-ttu-id="c408b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c408b-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c408b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c408b-137">Header</span></span><br/> | <dl> <span data-ttu-id="c408b-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c408b-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c408b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c408b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c408b-140">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c408b-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c408b-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="c408b-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
