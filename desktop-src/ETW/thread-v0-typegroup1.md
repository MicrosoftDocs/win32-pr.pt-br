---
description: Essa classe é a classe de tipo de evento para eventos de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Classe Thread_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967568"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="2e488-104">\_ \_ Classe TypeGroup1 de thread V0</span><span class="sxs-lookup"><span data-stu-id="2e488-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="2e488-105">Essa classe é a classe de tipo de evento para eventos de thread.</span><span class="sxs-lookup"><span data-stu-id="2e488-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="2e488-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="2e488-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e488-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e488-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="2e488-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2e488-108">Members</span></span>

<span data-ttu-id="2e488-109">A classe **thread \_ V0 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2e488-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="2e488-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e488-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e488-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e488-111">Properties</span></span>

<span data-ttu-id="2e488-112">A classe **thread \_ V0 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2e488-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e488-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="2e488-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e488-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e488-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e488-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e488-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e488-116">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="2e488-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="2e488-117">Identificador de processo do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="2e488-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="2e488-118">TThreadId</span><span class="sxs-lookup"><span data-stu-id="2e488-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e488-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e488-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e488-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e488-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e488-121">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="2e488-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="2e488-122">Identificador de thread do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="2e488-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e488-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e488-123">Requirements</span></span>



| <span data-ttu-id="2e488-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e488-124">Requirement</span></span> | <span data-ttu-id="2e488-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2e488-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2e488-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e488-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2e488-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2e488-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e488-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e488-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2e488-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2e488-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2e488-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e488-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e488-131">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="2e488-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




