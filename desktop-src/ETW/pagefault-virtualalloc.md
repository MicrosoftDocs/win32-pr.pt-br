---
description: Essa classe é a classe de tipo de evento para eventos de alocação virtual. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: Classe PageFault_VirtualAlloc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296449"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="f95cc-104">\_Classe falhadepágina VirtualAlloc</span><span class="sxs-lookup"><span data-stu-id="f95cc-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="f95cc-105">Essa classe é a classe de tipo de evento para eventos de alocação virtual.</span><span class="sxs-lookup"><span data-stu-id="f95cc-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="f95cc-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="f95cc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f95cc-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="f95cc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f95cc-108">Members</span></span>

<span data-ttu-id="f95cc-109">A classe **falhadepágina \_ VirtualAlloc** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f95cc-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="f95cc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f95cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f95cc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f95cc-111">Properties</span></span>

<span data-ttu-id="f95cc-112">A classe **falhadepágina \_ VirtualAlloc** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f95cc-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f95cc-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="f95cc-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95cc-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f95cc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f95cc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-116">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="f95cc-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f95cc-117">O endereço inicial no qual a memória foi alocada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="f95cc-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="f95cc-118">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="f95cc-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95cc-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f95cc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f95cc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-121">Qualificadores: WmiDataId (4), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="f95cc-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f95cc-122">O tipo de alocação de memória que foi executado.</span><span class="sxs-lookup"><span data-stu-id="f95cc-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="f95cc-123">Para obter os valores possíveis, consulte o parâmetro *flAllocationType* da função [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .</span><span class="sxs-lookup"><span data-stu-id="f95cc-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="f95cc-124">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="f95cc-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95cc-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f95cc-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f95cc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-127">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="f95cc-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f95cc-128">O processo que possui a memória (pode ser diferente do thread que realizou a alocação).</span><span class="sxs-lookup"><span data-stu-id="f95cc-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="f95cc-129">**Regiõesize**</span><span class="sxs-lookup"><span data-stu-id="f95cc-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95cc-130">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f95cc-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f95cc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95cc-132">Qualificadores: WmiDataId (2), extensão ("Tamanhot")</span><span class="sxs-lookup"><span data-stu-id="f95cc-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f95cc-133">O tamanho, em bytes, da memória que foi alocada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="f95cc-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f95cc-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f95cc-134">Requirements</span></span>



| <span data-ttu-id="f95cc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f95cc-135">Requirement</span></span> | <span data-ttu-id="f95cc-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f95cc-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f95cc-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f95cc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f95cc-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f95cc-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f95cc-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f95cc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f95cc-140">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f95cc-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f95cc-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f95cc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95cc-142">**Falhadepágina \_ v2**</span><span class="sxs-lookup"><span data-stu-id="f95cc-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
