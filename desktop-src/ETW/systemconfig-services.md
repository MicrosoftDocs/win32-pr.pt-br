---
description: Classe SystemConfig_Services-essa classe é a classe de tipo de evento para eventos de configuração de serviço.
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
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106054"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="10a11-103">Classe de serviços SystemConfigs \_</span><span class="sxs-lookup"><span data-stu-id="10a11-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="10a11-104">Essa classe é a classe de tipo de evento para eventos de configuração de serviço.</span><span class="sxs-lookup"><span data-stu-id="10a11-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="10a11-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="10a11-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a11-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10a11-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="10a11-107">Membros</span><span class="sxs-lookup"><span data-stu-id="10a11-107">Members</span></span>

<span data-ttu-id="10a11-108">A classe de **\_ Serviços SystemConfigs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10a11-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="10a11-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10a11-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10a11-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10a11-110">Properties</span></span>

<span data-ttu-id="10a11-111">A classe de **\_ Serviços SystemConfigs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10a11-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10a11-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="10a11-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a11-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10a11-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10a11-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10a11-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a11-115">Qualificadores: **WmiDataId** (5), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="10a11-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="10a11-116">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="10a11-116">Display name of the service.</span></span> <span data-ttu-id="10a11-117">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="10a11-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="10a11-118">No entanto, as comparações do nome para exibição nunca fazem diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="10a11-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="10a11-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="10a11-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a11-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10a11-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10a11-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10a11-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a11-122">Qualificadores: **WmiDataId** (1), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="10a11-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="10a11-123">Identificador do processo no qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="10a11-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="10a11-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="10a11-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a11-125">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10a11-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10a11-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10a11-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a11-127">Qualificadores: **WmiDataId** (6), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="10a11-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="10a11-128">Nome do processo no qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="10a11-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="10a11-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="10a11-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a11-130">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10a11-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10a11-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10a11-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a11-132">Qualificadores: **WmiDataId** (4), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="10a11-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="10a11-133">Identificador exclusivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="10a11-133">Unique identifier of the service.</span></span> <span data-ttu-id="10a11-134">O identificador fornece uma indicação da funcionalidade que o serviço fornece.</span><span class="sxs-lookup"><span data-stu-id="10a11-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="10a11-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="10a11-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a11-136">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10a11-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10a11-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10a11-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a11-138">Qualificadores: **WmiDataId** (2), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="10a11-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="10a11-139">Estado atual do serviço.</span><span class="sxs-lookup"><span data-stu-id="10a11-139">Current state of the service.</span></span> <span data-ttu-id="10a11-140">Para obter os valores possíveis, consulte o membro **dwCurrentState** do **processo de \_ status \_ do serviço**.</span><span class="sxs-lookup"><span data-stu-id="10a11-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="10a11-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="10a11-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a11-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10a11-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10a11-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10a11-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a11-144">Qualificadores: **WmiDataId** (3), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="10a11-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="10a11-145">Identifica o serviço.</span><span class="sxs-lookup"><span data-stu-id="10a11-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10a11-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10a11-146">Requirements</span></span>



| <span data-ttu-id="10a11-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="10a11-147">Requirement</span></span> | <span data-ttu-id="10a11-148">Valor</span><span class="sxs-lookup"><span data-stu-id="10a11-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10a11-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10a11-149">Minimum supported client</span></span><br/> | <span data-ttu-id="10a11-150">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10a11-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10a11-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10a11-151">Minimum supported server</span></span><br/> | <span data-ttu-id="10a11-152">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10a11-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10a11-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="10a11-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a11-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="10a11-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




