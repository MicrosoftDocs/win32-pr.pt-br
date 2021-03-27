---
description: Essa classe é a classe de tipo de evento para eventos de registro. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Classe Registry_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cd77ad0c12769c657b4e7c23c1fe1993a248481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827265"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="e5f0d-104">\_ \_ Classe TypeGroup1 do registro v1</span><span class="sxs-lookup"><span data-stu-id="e5f0d-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="e5f0d-105">Essa classe é a classe de tipo de evento para eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="e5f0d-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f0d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5f0d-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="e5f0d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e5f0d-108">Members</span></span>

<span data-ttu-id="e5f0d-109">A **classe \_ \_ TypeGroup1 do registro v1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5f0d-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e5f0d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5f0d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5f0d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5f0d-111">Properties</span></span>

<span data-ttu-id="e5f0d-112">A **classe \_ \_ TypeGroup1 do registro v1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5f0d-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="e5f0d-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5f0d-114">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5f0d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-116">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e5f0d-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e5f0d-117">Tempo decorrido da operação de registro.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5f0d-118">Índice</span><span class="sxs-lookup"><span data-stu-id="e5f0d-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5f0d-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5f0d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-121">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="e5f0d-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e5f0d-122">O índice de subchave para a operação de registro (como EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="e5f0d-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="e5f0d-123">Identificador de</span><span class="sxs-lookup"><span data-stu-id="e5f0d-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5f0d-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5f0d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-126">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="e5f0d-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e5f0d-127">Identificador para a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="e5f0d-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="e5f0d-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5f0d-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5f0d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-131">Qualificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="e5f0d-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e5f0d-132">Nome da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="e5f0d-133">Status</span><span class="sxs-lookup"><span data-stu-id="e5f0d-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5f0d-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5f0d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5f0d-136">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="e5f0d-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e5f0d-137">Valor de NTSTATUS da operação de registro.</span><span class="sxs-lookup"><span data-stu-id="e5f0d-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5f0d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5f0d-138">Requirements</span></span>



| <span data-ttu-id="e5f0d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5f0d-139">Requirement</span></span> | <span data-ttu-id="e5f0d-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e5f0d-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e5f0d-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5f0d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e5f0d-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5f0d-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e5f0d-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5f0d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e5f0d-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5f0d-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e5f0d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5f0d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f0d-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="e5f0d-147">**Registro \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e5f0d-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




