---
description: Essa classe é a classe de tipo de evento para eventos de falha de página. A sintaxe a seguir é simplificada do código MOF.
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
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829042"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="6f35d-104">\_Classe falhadepágina TransitionFault</span><span class="sxs-lookup"><span data-stu-id="6f35d-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="6f35d-105">Essa classe é a classe de tipo de evento para eventos de falha de página.</span><span class="sxs-lookup"><span data-stu-id="6f35d-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="6f35d-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="6f35d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f35d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f35d-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="6f35d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6f35d-108">Members</span></span>

<span data-ttu-id="6f35d-109">A classe **falhadepágina \_ TransitionFault** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f35d-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="6f35d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f35d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f35d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f35d-111">Properties</span></span>

<span data-ttu-id="6f35d-112">A classe **falhadepágina \_ TransitionFault** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f35d-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f35d-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="6f35d-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f35d-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f35d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f35d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f35d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f35d-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6f35d-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6f35d-117">Ponteiro para a instrução atual que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="6f35d-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="6f35d-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="6f35d-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f35d-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f35d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f35d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f35d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f35d-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6f35d-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6f35d-122">Endereço virtual da página que causou a falha de página.</span><span class="sxs-lookup"><span data-stu-id="6f35d-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f35d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f35d-123">Requirements</span></span>



| <span data-ttu-id="6f35d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f35d-124">Requirement</span></span> | <span data-ttu-id="6f35d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6f35d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6f35d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f35d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6f35d-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f35d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f35d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f35d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6f35d-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f35d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6f35d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f35d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f35d-131">**Falhadepágina \_ v2**</span><span class="sxs-lookup"><span data-stu-id="6f35d-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




