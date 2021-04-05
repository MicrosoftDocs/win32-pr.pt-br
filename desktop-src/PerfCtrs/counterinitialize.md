---
description: Registra o provedor e inicializa os conjuntos de contadores.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Função de reinicialização
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921750"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="27b4a-103">Função de reinicialização</span><span class="sxs-lookup"><span data-stu-id="27b4a-103">CounterInitialize function</span></span>

<span data-ttu-id="27b4a-104">Registra o provedor e inicializa os conjuntos de contadores.</span><span class="sxs-lookup"><span data-stu-id="27b4a-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27b4a-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="27b4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27b4a-106">Parameters</span></span>

<span data-ttu-id="27b4a-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="27b4a-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27b4a-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="27b4a-108">Return value</span></span>

<span data-ttu-id="27b4a-109">Retorna \_ o êxito do erro em caso de sucesso; caso contrário, um código de erro Win32 padrão.</span><span class="sxs-lookup"><span data-stu-id="27b4a-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b4a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="27b4a-110">Remarks</span></span>

<span data-ttu-id="27b4a-111">Seu provedor chama essa função.</span><span class="sxs-lookup"><span data-stu-id="27b4a-111">Your provider calls this function.</span></span> <span data-ttu-id="27b4a-112">A função inclui chamadas para a função [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) e a função [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="27b4a-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="27b4a-113">A ferramenta [**ctrpp**](ctrpp.md) gera essa função embutida quando você especifica o argumento **-o** .</span><span class="sxs-lookup"><span data-stu-id="27b4a-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="27b4a-114">O nome da função inclui uma cadeia de caracteres de *prefixo* se você especificar o argumento **-prefix** .</span><span class="sxs-lookup"><span data-stu-id="27b4a-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="27b4a-115">Se você especificar os argumentos **-MemoryRoutines** ou **-NotificationCallback** (ou especificar o atributo de **retorno de chamada** para o elemento [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), a assinatura de **metainicialização** será alterada para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="27b4a-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="27b4a-116">onde:</span><span class="sxs-lookup"><span data-stu-id="27b4a-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="27b4a-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span><span class="sxs-lookup"><span data-stu-id="27b4a-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="27b4a-118">O nome da função de retorno de chamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que você implementa para receber a notificação de solicitações de consumidor (por exemplo, solicitações para adicionar ou remover contadores da consulta).</span><span class="sxs-lookup"><span data-stu-id="27b4a-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="27b4a-119">Defina como **NULL** se você não implementar a função de retorno de chamada *ControlCallback* .</span><span class="sxs-lookup"><span data-stu-id="27b4a-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="27b4a-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span><span class="sxs-lookup"><span data-stu-id="27b4a-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="27b4a-121">O nome da função de retorno de chamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) que o PERFLIB chama para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="27b4a-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="27b4a-122">Defina como **NULL** se você não tiver especificado o argumento **-MemoryRoutines** .</span><span class="sxs-lookup"><span data-stu-id="27b4a-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="27b4a-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span><span class="sxs-lookup"><span data-stu-id="27b4a-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="27b4a-124">O nome da função de retorno de chamada [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) que o PERFLIB chama para liberar a memória alocada usando a função [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) .</span><span class="sxs-lookup"><span data-stu-id="27b4a-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="27b4a-125">Defina como **NULL** se *MemoryAllocationFunction* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="27b4a-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27b4a-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span><span class="sxs-lookup"><span data-stu-id="27b4a-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="27b4a-127">Informações de contexto a serem passadas para sua alocação de memória e rotinas gratuitas.</span><span class="sxs-lookup"><span data-stu-id="27b4a-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="27b4a-128">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="27b4a-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27b4a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27b4a-129">Requirements</span></span>



| <span data-ttu-id="27b4a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="27b4a-130">Requirement</span></span> | <span data-ttu-id="27b4a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="27b4a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="27b4a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27b4a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="27b4a-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="27b4a-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="27b4a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27b4a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="27b4a-135">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="27b4a-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

