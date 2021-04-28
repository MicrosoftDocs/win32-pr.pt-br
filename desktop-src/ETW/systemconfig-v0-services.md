---
description: Classe SystemConfig_V0_Services-essa classe é a classe de tipo de evento para eventos de configuração de serviço.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Classe SystemConfig_V0_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105924"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="35ec9-103">\_Classe de \_ Serviços SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="35ec9-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="35ec9-104">Essa classe é a classe de tipo de evento para eventos de configuração de serviço.</span><span class="sxs-lookup"><span data-stu-id="35ec9-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="35ec9-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="35ec9-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ec9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ec9-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="35ec9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="35ec9-107">Members</span></span>

<span data-ttu-id="35ec9-108">A classe **SystemConfig \_ V0 \_ Services** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="35ec9-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="35ec9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35ec9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35ec9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35ec9-110">Properties</span></span>

<span data-ttu-id="35ec9-111">A classe **SystemConfig \_ V0 \_ Services** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="35ec9-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35ec9-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="35ec9-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ec9-113">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="35ec9-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35ec9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-115">Qualificadores: **WmiDataId** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="35ec9-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="35ec9-116">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="35ec9-116">Display name of the service.</span></span> <span data-ttu-id="35ec9-117">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="35ec9-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="35ec9-118">No entanto, as comparações do nome para exibição nunca fazem diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="35ec9-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="35ec9-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="35ec9-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ec9-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35ec9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35ec9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-122">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="35ec9-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="35ec9-123">Identificador do processo no qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="35ec9-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="35ec9-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="35ec9-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ec9-125">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="35ec9-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35ec9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-127">Qualificadores: **WmiDataId** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="35ec9-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="35ec9-128">Nome do processo no qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="35ec9-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="35ec9-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="35ec9-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ec9-130">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="35ec9-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35ec9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ec9-132">Qualificadores: **WmiDataId** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="35ec9-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="35ec9-133">Identificador exclusivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="35ec9-133">Unique identifier of the service.</span></span> <span data-ttu-id="35ec9-134">O identificador fornece uma indicação da funcionalidade que o serviço fornece.</span><span class="sxs-lookup"><span data-stu-id="35ec9-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35ec9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ec9-135">Requirements</span></span>



| <span data-ttu-id="35ec9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ec9-136">Requirement</span></span> | <span data-ttu-id="35ec9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="35ec9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35ec9-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35ec9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="35ec9-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="35ec9-139">None supported</span></span><br/>                            |
| <span data-ttu-id="35ec9-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35ec9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="35ec9-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35ec9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35ec9-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="35ec9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ec9-143">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="35ec9-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




