---
description: Representa uma especialização da Associação de componente do sistema que estabelece que o pool de recursos é definido no contexto do sistema.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Classe Msvm_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826865"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="db012-103">\_Classe Msvm HostedResourcePool</span><span class="sxs-lookup"><span data-stu-id="db012-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="db012-104">Representa uma especialização da Associação de componente do sistema que estabelece que o pool de recursos é definido no contexto do sistema.</span><span class="sxs-lookup"><span data-stu-id="db012-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="db012-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="db012-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="db012-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db012-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="db012-107">Membros</span><span class="sxs-lookup"><span data-stu-id="db012-107">Members</span></span>

<span data-ttu-id="db012-108">A classe **Msvm \_ HostedResourcePool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="db012-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="db012-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="db012-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db012-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="db012-110">Properties</span></span>

<span data-ttu-id="db012-111">A classe **Msvm \_ HostedResourcePool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="db012-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db012-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="db012-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db012-113">Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="db012-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="db012-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db012-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db012-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="db012-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="db012-116">O sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="db012-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="db012-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="db012-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db012-118">Tipo de dados: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="db012-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="db012-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db012-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db012-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="db012-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="db012-121">O pool de recursos que é um componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="db012-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db012-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db012-122">Requirements</span></span>



| <span data-ttu-id="db012-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="db012-123">Requirement</span></span> | <span data-ttu-id="db012-124">Valor</span><span class="sxs-lookup"><span data-stu-id="db012-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db012-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db012-125">Minimum supported client</span></span><br/> | <span data-ttu-id="db012-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="db012-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="db012-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db012-127">Minimum supported server</span></span><br/> | <span data-ttu-id="db012-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="db012-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db012-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="db012-129">Namespace</span></span><br/>                | <span data-ttu-id="db012-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="db012-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="db012-131">MOF</span><span class="sxs-lookup"><span data-stu-id="db012-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db012-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db012-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="db012-133">DLL</span><span class="sxs-lookup"><span data-stu-id="db012-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db012-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db012-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

