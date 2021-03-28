---
description: Representa a classe de tipo de evento para criação de identificador ou eventos de fechamento.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Classe ObHandleEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968041"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="48433-103">Classe ObHandleEvent</span><span class="sxs-lookup"><span data-stu-id="48433-103">ObHandleEvent class</span></span>

<span data-ttu-id="48433-104">Representa a classe de tipo de evento para criação de identificador ou eventos de fechamento.</span><span class="sxs-lookup"><span data-stu-id="48433-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="48433-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="48433-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48433-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48433-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="48433-107">Membros</span><span class="sxs-lookup"><span data-stu-id="48433-107">Members</span></span>

<span data-ttu-id="48433-108">A classe **ObHandleEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="48433-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="48433-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48433-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48433-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48433-110">Properties</span></span>

<span data-ttu-id="48433-111">A classe **ObHandleEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48433-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48433-112">**Handle**</span><span class="sxs-lookup"><span data-stu-id="48433-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48433-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48433-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48433-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48433-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48433-115">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="48433-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="48433-116">O identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="48433-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="48433-117">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="48433-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48433-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48433-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48433-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48433-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48433-120">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="48433-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="48433-121">O objeto.</span><span class="sxs-lookup"><span data-stu-id="48433-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="48433-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="48433-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48433-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48433-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48433-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48433-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48433-125">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="48433-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="48433-126">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="48433-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="48433-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="48433-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48433-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48433-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48433-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48433-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48433-130">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="48433-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="48433-131">O tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="48433-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48433-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48433-132">Requirements</span></span>



| <span data-ttu-id="48433-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="48433-133">Requirement</span></span> | <span data-ttu-id="48433-134">Valor</span><span class="sxs-lookup"><span data-stu-id="48433-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48433-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48433-135">Minimum supported client</span></span><br/> | <span data-ttu-id="48433-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="48433-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48433-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48433-137">Minimum supported server</span></span><br/> | <span data-ttu-id="48433-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="48433-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48433-139">MOF</span><span class="sxs-lookup"><span data-stu-id="48433-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48433-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48433-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




