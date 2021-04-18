---
title: DXCoreAdapterMemoryBudget
description: Descreve o orçamento de memória para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454303"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="3fee9-103">Estrutura DXCoreAdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="3fee9-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="3fee9-104">Especifica o estado do adaptador <em>AdapterMemoryBudget</em> , que recupera ou solicita o orçamento de memória do adaptador no adaptador.</span><span class="sxs-lookup"><span data-stu-id="3fee9-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="3fee9-105">A configuração (solicitando) um orçamento representa a memória física mínima necessária a ser reservada, em bytes, no adaptador.</span><span class="sxs-lookup"><span data-stu-id="3fee9-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="3fee9-106">Recomendamos que você defina uma reserva de adaptador para denotar a quantidade de memória física que seu aplicativo não pode acessar sem.</span><span class="sxs-lookup"><span data-stu-id="3fee9-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="3fee9-107">Esse valor ajuda o sistema operacional (SO) a minimizar rapidamente o impacto de grandes situações de pressão de memória.</span><span class="sxs-lookup"><span data-stu-id="3fee9-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="3fee9-108">Ao chamar [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), o estado do adaptador <em>AdapterMemoryBudget</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* e o tipo **DXCoreAdapterMemoryBudget** para *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="3fee9-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="3fee9-109">Ao chamar [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), o estado do adaptador <em>AdapterMemoryBudget</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* e o tipo **uint64_t** para *inputData*.</span><span class="sxs-lookup"><span data-stu-id="3fee9-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fee9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fee9-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="3fee9-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3fee9-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="3fee9-112">visto</span><span class="sxs-lookup"><span data-stu-id="3fee9-112">budget</span></span>

<span data-ttu-id="3fee9-113">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="3fee9-113">Type: **uint64_t**</span></span>

<span data-ttu-id="3fee9-114">Especifica o orçamento de memória do adaptador fornecido pelo sistema operacional, em bytes, que seu aplicativo deve ter como destino.</span><span class="sxs-lookup"><span data-stu-id="3fee9-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="3fee9-115">Se *currentUsage* for maior que o *orçamento*, seu aplicativo poderá incorrer em penalidades de desempenho ou em virtude da atividade em segundo plano pelo sistema operacional, que tem o objetivo de fornecer a outros aplicativos um uso justo da memória do adaptador.</span><span class="sxs-lookup"><span data-stu-id="3fee9-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="3fee9-116">currentUsage</span><span class="sxs-lookup"><span data-stu-id="3fee9-116">currentUsage</span></span>

<span data-ttu-id="3fee9-117">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="3fee9-117">Type: **uint64_t**</span></span>

<span data-ttu-id="3fee9-118">Especifica o uso de memória do adaptador atual do aplicativo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3fee9-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="3fee9-119">availableForReservation</span><span class="sxs-lookup"><span data-stu-id="3fee9-119">availableForReservation</span></span>

<span data-ttu-id="3fee9-120">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="3fee9-120">Type: **uint64_t**</span></span>

<span data-ttu-id="3fee9-121">Especifica a quantidade de memória do adaptador, em bytes, que seu aplicativo está disponível para reserva.</span><span class="sxs-lookup"><span data-stu-id="3fee9-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="3fee9-122">Para reservar essa memória do adaptador, o aplicativo deve chamar [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) com o *estado* definido como [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span><span class="sxs-lookup"><span data-stu-id="3fee9-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="3fee9-123">currentReservation</span><span class="sxs-lookup"><span data-stu-id="3fee9-123">currentReservation</span></span>

<span data-ttu-id="3fee9-124">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="3fee9-124">Type: **uint64_t**</span></span>

<span data-ttu-id="3fee9-125">Especifica a quantidade de memória do adaptador, em bytes, reservada pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3fee9-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="3fee9-126">O sistema operacional usa a reserva como uma dica para determinar o conjunto de trabalho mínimo de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3fee9-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="3fee9-127">Seu aplicativo deve tentar garantir que o uso de memória do adaptador possa ser cortado para atender a esse requisito.</span><span class="sxs-lookup"><span data-stu-id="3fee9-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fee9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fee9-128">See also</span></span>

<span data-ttu-id="3fee9-129">[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="3fee9-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>