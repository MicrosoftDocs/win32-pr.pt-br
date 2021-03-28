---
description: Essa classe é a classe de tipo de evento para eventos de rastreamento de pilha.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Classe StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968033"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="00b70-103">\_Classe de evento StackWalk</span><span class="sxs-lookup"><span data-stu-id="00b70-103">StackWalk\_Event class</span></span>

<span data-ttu-id="00b70-104">Essa classe é a classe de tipo de evento para eventos de rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="00b70-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="00b70-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="00b70-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b70-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00b70-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="00b70-107">Membros</span><span class="sxs-lookup"><span data-stu-id="00b70-107">Members</span></span>

<span data-ttu-id="00b70-108">A classe de **\_ evento StackWalk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="00b70-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="00b70-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00b70-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00b70-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00b70-110">Properties</span></span>

<span data-ttu-id="00b70-111">A classe de **\_ evento StackWalk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="00b70-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00b70-112">**EventTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="00b70-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b70-113">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00b70-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00b70-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00b70-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00b70-115">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="00b70-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="00b70-116">Carimbo de data/hora do evento original do cabeçalho do evento.</span><span class="sxs-lookup"><span data-stu-id="00b70-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="00b70-117">Use este carimbo de data/hora para corresponder a pilha a um evento.</span><span class="sxs-lookup"><span data-stu-id="00b70-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="00b70-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="00b70-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b70-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00b70-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00b70-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00b70-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00b70-121">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="00b70-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="00b70-122">Endereço da chamada.</span><span class="sxs-lookup"><span data-stu-id="00b70-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="00b70-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="00b70-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b70-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00b70-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00b70-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00b70-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00b70-126">Qualificadores: WmiDataId (195), ponteiro</span><span class="sxs-lookup"><span data-stu-id="00b70-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="00b70-127">Endereço da chamada.</span><span class="sxs-lookup"><span data-stu-id="00b70-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="00b70-128">**StackProcess**</span><span class="sxs-lookup"><span data-stu-id="00b70-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b70-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00b70-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00b70-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00b70-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00b70-131">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="00b70-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="00b70-132">O identificador de processo do evento original.</span><span class="sxs-lookup"><span data-stu-id="00b70-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="00b70-133">**StackThread**</span><span class="sxs-lookup"><span data-stu-id="00b70-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b70-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00b70-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00b70-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00b70-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00b70-136">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="00b70-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="00b70-137">O identificador de thread do evento original.</span><span class="sxs-lookup"><span data-stu-id="00b70-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00b70-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="00b70-138">Remarks</span></span>

<span data-ttu-id="00b70-139">Observe que a classe não mostra todas as propriedades **Stack \* n**\* que existem entre **Stack1** e **Stack192**.</span><span class="sxs-lookup"><span data-stu-id="00b70-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="00b70-140">Use o tamanho do evento para determinar quantas propriedades **Stack \* n**\* contêm endereços válidos.</span><span class="sxs-lookup"><span data-stu-id="00b70-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="00b70-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00b70-141">Requirements</span></span>



| <span data-ttu-id="00b70-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b70-142">Requirement</span></span> | <span data-ttu-id="00b70-143">Valor</span><span class="sxs-lookup"><span data-stu-id="00b70-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="00b70-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00b70-144">Minimum supported client</span></span><br/> | <span data-ttu-id="00b70-145">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00b70-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="00b70-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00b70-146">Minimum supported server</span></span><br/> | <span data-ttu-id="00b70-147">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="00b70-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




