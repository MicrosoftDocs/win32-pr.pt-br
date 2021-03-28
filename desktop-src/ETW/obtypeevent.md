---
description: Representa a classe de tipo de evento para eventos de tipo de objeto relacionados ao início e ao fim da coleta de dados.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Classe ObTypeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091737"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="0b267-103">Classe ObTypeEvent</span><span class="sxs-lookup"><span data-stu-id="0b267-103">ObTypeEvent class</span></span>

<span data-ttu-id="0b267-104">Representa a classe de tipo de evento para eventos de tipo de objeto relacionados ao início e ao fim da coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="0b267-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="0b267-105">Esse evento envolve o mapeamento dos valores de índice de tipo para os nomes de tipo.</span><span class="sxs-lookup"><span data-stu-id="0b267-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="0b267-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b267-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b267-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b267-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="0b267-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0b267-108">Members</span></span>

<span data-ttu-id="0b267-109">A classe **ObTypeEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b267-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="0b267-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b267-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b267-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b267-111">Properties</span></span>

<span data-ttu-id="0b267-112">A classe **ObTypeEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b267-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b267-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="0b267-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b267-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b267-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b267-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b267-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b267-116">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="0b267-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0b267-117">O tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="0b267-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="0b267-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="0b267-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b267-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b267-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b267-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b267-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b267-121">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="0b267-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="0b267-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0b267-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0b267-123">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="0b267-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b267-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b267-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b267-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b267-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b267-126">Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="0b267-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="0b267-127">O nome do tipo.</span><span class="sxs-lookup"><span data-stu-id="0b267-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b267-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b267-128">Requirements</span></span>



| <span data-ttu-id="0b267-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b267-129">Requirement</span></span> | <span data-ttu-id="0b267-130">Valor</span><span class="sxs-lookup"><span data-stu-id="0b267-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b267-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b267-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0b267-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0b267-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b267-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b267-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0b267-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0b267-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b267-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0b267-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b267-136"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b267-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




