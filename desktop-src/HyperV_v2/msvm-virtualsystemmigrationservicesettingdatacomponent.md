---
description: Uma associação usada para representar as configurações de rede de migração do sistema virtual do serviço de migração do sistema virtual.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Classe Msvm_VirtualSystemMigrationServiceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769209"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="8149e-103">\_Classe Msvm VirtualSystemMigrationServiceSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="8149e-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="8149e-104">Uma associação usada para representar as configurações de rede de migração do sistema virtual do serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8149e-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="8149e-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8149e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8149e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8149e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8149e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8149e-107">Members</span></span>

<span data-ttu-id="8149e-108">A classe **Msvm \_ VirtualSystemMigrationServiceSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8149e-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8149e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8149e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8149e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8149e-110">Properties</span></span>

<span data-ttu-id="8149e-111">A classe **Msvm \_ VirtualSystemMigrationServiceSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8149e-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8149e-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8149e-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8149e-113">Tipo de dados: **Msvm \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="8149e-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="8149e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8149e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8149e-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8149e-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8149e-116">Uma referência a uma instância da classe [**Msvm \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) que representa as configurações do serviço de migração.</span><span class="sxs-lookup"><span data-stu-id="8149e-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="8149e-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8149e-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8149e-118">Tipo de dados: **Msvm \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="8149e-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="8149e-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8149e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8149e-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8149e-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8149e-121">Uma referência a uma instância da classe [**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que representa as configurações de rede de migração.</span><span class="sxs-lookup"><span data-stu-id="8149e-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8149e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8149e-122">Requirements</span></span>



| <span data-ttu-id="8149e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8149e-123">Requirement</span></span> | <span data-ttu-id="8149e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8149e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8149e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8149e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8149e-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8149e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8149e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8149e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8149e-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8149e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8149e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8149e-129">Namespace</span></span><br/>                | <span data-ttu-id="8149e-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8149e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8149e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8149e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8149e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8149e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8149e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8149e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8149e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8149e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

