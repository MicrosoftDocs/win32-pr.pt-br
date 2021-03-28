---
description: Representa a classe de tipo de evento para eventos de identificador de objeto relacionados ao início e ao fim da coleta de dados.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Classe ObHandleRundownEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968042"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="f47f7-103">Classe ObHandleRundownEvent</span><span class="sxs-lookup"><span data-stu-id="f47f7-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="f47f7-104">Representa a classe de tipo de evento para eventos de identificador de objeto relacionados ao início e ao fim da coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="f47f7-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="f47f7-105">Esse evento envolve a enumeração de todos os identificadores quando o encerramento é executado.</span><span class="sxs-lookup"><span data-stu-id="f47f7-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="f47f7-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f47f7-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f47f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f47f7-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="f47f7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f47f7-108">Members</span></span>

<span data-ttu-id="f47f7-109">A classe **ObHandleRundownEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f47f7-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f47f7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f47f7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f47f7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f47f7-111">Properties</span></span>

<span data-ttu-id="f47f7-112">A classe **ObHandleRundownEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f47f7-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f47f7-113">**Handle**</span><span class="sxs-lookup"><span data-stu-id="f47f7-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47f7-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47f7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47f7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-116">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="f47f7-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="f47f7-117">O identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="f47f7-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="f47f7-118">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="f47f7-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47f7-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47f7-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47f7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-121">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="f47f7-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f47f7-122">O objeto.</span><span class="sxs-lookup"><span data-stu-id="f47f7-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="f47f7-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="f47f7-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47f7-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47f7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47f7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-126">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="f47f7-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="f47f7-127">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="f47f7-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="f47f7-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="f47f7-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47f7-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f47f7-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47f7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-131">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="f47f7-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="f47f7-132">O tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="f47f7-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="f47f7-133">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="f47f7-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47f7-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47f7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47f7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47f7-136">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="f47f7-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="f47f7-137">O identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="f47f7-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f47f7-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f47f7-138">Requirements</span></span>



| <span data-ttu-id="f47f7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f47f7-139">Requirement</span></span> | <span data-ttu-id="f47f7-140">Valor</span><span class="sxs-lookup"><span data-stu-id="f47f7-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f47f7-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f47f7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f47f7-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f47f7-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f47f7-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f47f7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f47f7-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f47f7-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f47f7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f47f7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f47f7-146"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f47f7-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




