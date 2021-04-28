---
description: Classe Registry_V0_TypeGroup1-essa classe é a classe de tipo de evento para eventos de registro. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Classe Registry_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106184"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="498c8-104">\_Classe V0 \_ TypeGroup1 do registro</span><span class="sxs-lookup"><span data-stu-id="498c8-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="498c8-105">Essa classe é a classe de tipo de evento para eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="498c8-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="498c8-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="498c8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="498c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="498c8-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="498c8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="498c8-108">Members</span></span>

<span data-ttu-id="498c8-109">A **classe \_ V0 \_ TypeGroup1 do registro** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="498c8-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="498c8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="498c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="498c8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="498c8-111">Properties</span></span>

<span data-ttu-id="498c8-112">A **classe \_ V0 \_ TypeGroup1 do registro** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="498c8-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="498c8-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="498c8-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498c8-114">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="498c8-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="498c8-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="498c8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498c8-116">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="498c8-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="498c8-117">Tempo decorrido da operação de registro.</span><span class="sxs-lookup"><span data-stu-id="498c8-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="498c8-118">Identificador de</span><span class="sxs-lookup"><span data-stu-id="498c8-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498c8-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="498c8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="498c8-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="498c8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498c8-121">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="498c8-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="498c8-122">Identificador para a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="498c8-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="498c8-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="498c8-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498c8-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="498c8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="498c8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="498c8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498c8-126">Qualificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="498c8-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="498c8-127">Nome da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="498c8-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="498c8-128">Status</span><span class="sxs-lookup"><span data-stu-id="498c8-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="498c8-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="498c8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="498c8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="498c8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="498c8-131">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="498c8-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="498c8-132">Valor de NTSTATUS da operação de registro.</span><span class="sxs-lookup"><span data-stu-id="498c8-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="498c8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="498c8-133">Requirements</span></span>



| <span data-ttu-id="498c8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="498c8-134">Requirement</span></span> | <span data-ttu-id="498c8-135">Valor</span><span class="sxs-lookup"><span data-stu-id="498c8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="498c8-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="498c8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="498c8-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="498c8-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="498c8-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="498c8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="498c8-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="498c8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="498c8-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="498c8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="498c8-141">**V0 do registro \_**</span><span class="sxs-lookup"><span data-stu-id="498c8-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




