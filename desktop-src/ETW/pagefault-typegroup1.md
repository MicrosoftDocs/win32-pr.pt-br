---
description: Classe PageFault_TypeGroup1-essa classe é a classe de tipo de evento para eventos de falha de página. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: Classe PageFault_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106404"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="5b67a-104">\_Classe falhadepágina TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="5b67a-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="5b67a-105">Essa classe é a classe de tipo de evento para eventos de falha de página.</span><span class="sxs-lookup"><span data-stu-id="5b67a-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="5b67a-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5b67a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b67a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b67a-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="5b67a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5b67a-108">Members</span></span>

<span data-ttu-id="5b67a-109">A classe **falhadepágina \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b67a-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="5b67a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b67a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b67a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b67a-111">Properties</span></span>

<span data-ttu-id="5b67a-112">A classe **falhadepágina \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b67a-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b67a-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="5b67a-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b67a-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b67a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b67a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b67a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b67a-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5b67a-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5b67a-117">Ponteiro para a instrução atual que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="5b67a-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="5b67a-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="5b67a-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b67a-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b67a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b67a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b67a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b67a-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5b67a-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5b67a-122">Endereço virtual da página que causou a falha de página.</span><span class="sxs-lookup"><span data-stu-id="5b67a-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b67a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b67a-123">Remarks</span></span>

<span data-ttu-id="5b67a-124">Uma falha de página ocorre quando uma página procurada no cache de memória não é encontrada e deve ser recuperada de outro lugar na memória (uma falha de software) ou do disco (uma falha rígida).</span><span class="sxs-lookup"><span data-stu-id="5b67a-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b67a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b67a-125">Requirements</span></span>



| <span data-ttu-id="5b67a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b67a-126">Requirement</span></span> | <span data-ttu-id="5b67a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5b67a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b67a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b67a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5b67a-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b67a-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5b67a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b67a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5b67a-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b67a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b67a-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5b67a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b67a-133">**Falhadepágina \_ v2**</span><span class="sxs-lookup"><span data-stu-id="5b67a-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




