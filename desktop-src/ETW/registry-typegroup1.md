---
description: Classe Registry_TypeGroup1-essa classe é a classe de tipo de evento para eventos de registro. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Classe Registry_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: d86412a950246bee4f9a692ab80e91b99d945c20
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106244"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="00575-104">\_Classe TypeGroup1 do registro</span><span class="sxs-lookup"><span data-stu-id="00575-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="00575-105">Essa classe é a classe de tipo de evento para eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="00575-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="00575-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="00575-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="00575-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00575-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="00575-108">Membros</span><span class="sxs-lookup"><span data-stu-id="00575-108">Members</span></span>

<span data-ttu-id="00575-109">A **classe \_ TypeGroup1 do registro** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="00575-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="00575-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00575-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00575-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00575-111">Properties</span></span>

<span data-ttu-id="00575-112">A **classe \_ TypeGroup1 do registro** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="00575-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00575-113">Índice</span><span class="sxs-lookup"><span data-stu-id="00575-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00575-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00575-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00575-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00575-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00575-116">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="00575-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="00575-117">O índice de subchave para a operação de registro (como EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="00575-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="00575-118">Inicialtime</span><span class="sxs-lookup"><span data-stu-id="00575-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00575-119">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="00575-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="00575-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00575-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00575-121">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="00575-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="00575-122">Hora inicial da operação de registro.</span><span class="sxs-lookup"><span data-stu-id="00575-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="00575-123">Identificador de</span><span class="sxs-lookup"><span data-stu-id="00575-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00575-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00575-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00575-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00575-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00575-126">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="00575-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="00575-127">Identificador para a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="00575-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="00575-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="00575-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00575-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00575-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00575-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00575-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00575-131">Qualificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="00575-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="00575-132">Nome da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="00575-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="00575-133">Status</span><span class="sxs-lookup"><span data-stu-id="00575-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00575-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00575-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00575-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00575-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00575-136">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="00575-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="00575-137">Valor de NTSTATUS da operação de registro.</span><span class="sxs-lookup"><span data-stu-id="00575-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00575-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00575-138">Requirements</span></span>



| <span data-ttu-id="00575-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="00575-139">Requirement</span></span> | <span data-ttu-id="00575-140">Valor</span><span class="sxs-lookup"><span data-stu-id="00575-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="00575-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00575-141">Minimum supported client</span></span><br/> | <span data-ttu-id="00575-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00575-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="00575-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00575-143">Minimum supported server</span></span><br/> | <span data-ttu-id="00575-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00575-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="00575-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="00575-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00575-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="00575-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




