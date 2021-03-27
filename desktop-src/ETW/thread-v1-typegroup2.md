---
description: Essa classe é a classe de tipo de evento para eventos de término de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Classe Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502068"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="08819-104">\_ \_ Classe TypeGroup2 de thread v1</span><span class="sxs-lookup"><span data-stu-id="08819-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="08819-105">Essa classe é a classe de tipo de evento para eventos de término de thread.</span><span class="sxs-lookup"><span data-stu-id="08819-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="08819-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="08819-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="08819-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08819-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="08819-108">Membros</span><span class="sxs-lookup"><span data-stu-id="08819-108">Members</span></span>

<span data-ttu-id="08819-109">A classe **thread \_ v1 \_ TypeGroup2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08819-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="08819-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08819-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08819-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08819-111">Properties</span></span>

<span data-ttu-id="08819-112">A classe **thread \_ v1 \_ TypeGroup2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08819-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08819-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="08819-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08819-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08819-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08819-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08819-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08819-116">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="08819-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="08819-117">Identificador de processo do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="08819-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="08819-118">**Windows Server 2003:** Contém o qualificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="08819-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="08819-119">TThreadId</span><span class="sxs-lookup"><span data-stu-id="08819-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08819-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08819-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08819-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08819-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08819-122">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="08819-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="08819-123">Identificador de thread do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="08819-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="08819-124">**Windows Server 2003:** Contém o qualificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="08819-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08819-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08819-125">Requirements</span></span>



| <span data-ttu-id="08819-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="08819-126">Requirement</span></span> | <span data-ttu-id="08819-127">Valor</span><span class="sxs-lookup"><span data-stu-id="08819-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="08819-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08819-128">Minimum supported client</span></span><br/> | <span data-ttu-id="08819-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08819-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="08819-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08819-130">Minimum supported server</span></span><br/> | <span data-ttu-id="08819-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08819-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08819-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="08819-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08819-133">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="08819-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




