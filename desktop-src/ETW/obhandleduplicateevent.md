---
description: Representa a classe de tipo de evento para manipular eventos de duplicação.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Classe ObHandleDuplicateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968184"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="51abb-103">Classe ObHandleDuplicateEvent</span><span class="sxs-lookup"><span data-stu-id="51abb-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="51abb-104">Representa a classe de tipo de evento para manipular eventos de duplicação.</span><span class="sxs-lookup"><span data-stu-id="51abb-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="51abb-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="51abb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51abb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51abb-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="51abb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="51abb-107">Members</span></span>

<span data-ttu-id="51abb-108">A classe **ObHandleDuplicateEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="51abb-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="51abb-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51abb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51abb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51abb-110">Properties</span></span>

<span data-ttu-id="51abb-111">A classe **ObHandleDuplicateEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="51abb-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51abb-112">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="51abb-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51abb-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51abb-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51abb-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51abb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51abb-115">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="51abb-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="51abb-116">O objeto.</span><span class="sxs-lookup"><span data-stu-id="51abb-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="51abb-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="51abb-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51abb-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51abb-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51abb-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51abb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51abb-120">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="51abb-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="51abb-121">O tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="51abb-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="51abb-122">**SourceHandle**</span><span class="sxs-lookup"><span data-stu-id="51abb-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51abb-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51abb-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51abb-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51abb-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51abb-125">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="51abb-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="51abb-126">O identificador do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="51abb-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="51abb-127">**TargetHandle**</span><span class="sxs-lookup"><span data-stu-id="51abb-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51abb-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51abb-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51abb-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51abb-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51abb-130">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="51abb-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="51abb-131">O identificador do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="51abb-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="51abb-132">**TargetProcessId**</span><span class="sxs-lookup"><span data-stu-id="51abb-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51abb-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51abb-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51abb-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51abb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51abb-135">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="51abb-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="51abb-136">O identificador do processo do destino.</span><span class="sxs-lookup"><span data-stu-id="51abb-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51abb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51abb-137">Requirements</span></span>



| <span data-ttu-id="51abb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="51abb-138">Requirement</span></span> | <span data-ttu-id="51abb-139">Valor</span><span class="sxs-lookup"><span data-stu-id="51abb-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51abb-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51abb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="51abb-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="51abb-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="51abb-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51abb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="51abb-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="51abb-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51abb-144">MOF</span><span class="sxs-lookup"><span data-stu-id="51abb-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51abb-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51abb-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




