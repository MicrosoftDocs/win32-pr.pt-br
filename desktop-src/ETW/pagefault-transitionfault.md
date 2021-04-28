---
description: Classe PageFault_TransitionFault-essa classe é a classe de tipo de evento para eventos de falha de página. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: Classe PageFault_TransitionFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c8ee12cf201b9ee83d231bf1f5e499550aa3cd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106454"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="84ab0-104">\_Classe falhadepágina TransitionFault</span><span class="sxs-lookup"><span data-stu-id="84ab0-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="84ab0-105">Essa classe é a classe de tipo de evento para eventos de falha de página.</span><span class="sxs-lookup"><span data-stu-id="84ab0-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="84ab0-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="84ab0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ab0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84ab0-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="84ab0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="84ab0-108">Members</span></span>

<span data-ttu-id="84ab0-109">A classe **falhadepágina \_ TransitionFault** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="84ab0-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="84ab0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84ab0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84ab0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84ab0-111">Properties</span></span>

<span data-ttu-id="84ab0-112">A classe **falhadepágina \_ TransitionFault** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="84ab0-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84ab0-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="84ab0-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84ab0-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84ab0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84ab0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="84ab0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84ab0-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="84ab0-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="84ab0-117">Ponteiro para a instrução atual que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="84ab0-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="84ab0-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="84ab0-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84ab0-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84ab0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84ab0-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="84ab0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84ab0-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="84ab0-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="84ab0-122">Endereço virtual da página que causou a falha de página.</span><span class="sxs-lookup"><span data-stu-id="84ab0-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84ab0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84ab0-123">Requirements</span></span>



| <span data-ttu-id="84ab0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="84ab0-124">Requirement</span></span> | <span data-ttu-id="84ab0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="84ab0-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="84ab0-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84ab0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84ab0-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="84ab0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="84ab0-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84ab0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84ab0-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="84ab0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="84ab0-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="84ab0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ab0-131">**Falhadepágina \_ v2**</span><span class="sxs-lookup"><span data-stu-id="84ab0-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




