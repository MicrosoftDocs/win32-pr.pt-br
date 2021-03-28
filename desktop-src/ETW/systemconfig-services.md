---
description: Essa classe é a classe de tipo de evento para eventos de configuração de serviço.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Classe SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97b4d2a56f2ed739403681875e0be4d9e21481ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967380"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="59a2c-103">Classe de serviços SystemConfigs \_</span><span class="sxs-lookup"><span data-stu-id="59a2c-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="59a2c-104">Essa classe é a classe de tipo de evento para eventos de configuração de serviço.</span><span class="sxs-lookup"><span data-stu-id="59a2c-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="59a2c-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="59a2c-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a2c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59a2c-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="59a2c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="59a2c-107">Members</span></span>

<span data-ttu-id="59a2c-108">A classe de **\_ Serviços SystemConfigs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59a2c-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="59a2c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59a2c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59a2c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59a2c-110">Properties</span></span>

<span data-ttu-id="59a2c-111">A classe de **\_ Serviços SystemConfigs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="59a2c-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59a2c-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="59a2c-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a2c-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="59a2c-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59a2c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-115">Qualificadores: **WmiDataId** (5), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="59a2c-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="59a2c-116">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="59a2c-116">Display name of the service.</span></span> <span data-ttu-id="59a2c-117">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="59a2c-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="59a2c-118">No entanto, as comparações do nome para exibição nunca fazem diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="59a2c-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="59a2c-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="59a2c-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a2c-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59a2c-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59a2c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-122">Qualificadores: **WmiDataId** (1), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="59a2c-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="59a2c-123">Identificador do processo no qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="59a2c-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="59a2c-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="59a2c-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a2c-125">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="59a2c-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59a2c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-127">Qualificadores: **WmiDataId** (6), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="59a2c-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="59a2c-128">Nome do processo no qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="59a2c-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="59a2c-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="59a2c-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a2c-130">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="59a2c-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59a2c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-132">Qualificadores: **WmiDataId** (4), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="59a2c-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="59a2c-133">Identificador exclusivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="59a2c-133">Unique identifier of the service.</span></span> <span data-ttu-id="59a2c-134">O identificador fornece uma indicação da funcionalidade que o serviço fornece.</span><span class="sxs-lookup"><span data-stu-id="59a2c-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="59a2c-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="59a2c-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a2c-136">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59a2c-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59a2c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-138">Qualificadores: **WmiDataId** (2), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="59a2c-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="59a2c-139">Estado atual do serviço.</span><span class="sxs-lookup"><span data-stu-id="59a2c-139">Current state of the service.</span></span> <span data-ttu-id="59a2c-140">Para obter os valores possíveis, consulte o membro **dwCurrentState** do **processo de \_ status \_ do serviço**.</span><span class="sxs-lookup"><span data-stu-id="59a2c-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="59a2c-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="59a2c-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a2c-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59a2c-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59a2c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a2c-144">Qualificadores: **WmiDataId** (3), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="59a2c-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="59a2c-145">Identifica o serviço.</span><span class="sxs-lookup"><span data-stu-id="59a2c-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59a2c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59a2c-146">Requirements</span></span>



| <span data-ttu-id="59a2c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a2c-147">Requirement</span></span> | <span data-ttu-id="59a2c-148">Valor</span><span class="sxs-lookup"><span data-stu-id="59a2c-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59a2c-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59a2c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="59a2c-150">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59a2c-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59a2c-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59a2c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="59a2c-152">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59a2c-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59a2c-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="59a2c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a2c-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="59a2c-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




