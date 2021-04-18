---
description: Associa uma instância da classe Msvm \_ ComputerSystem ou Msvm \_ PlannedComputerSystem que representa um sistema virtual, com uma instância da classe Msvm \_ VirtualSystemSettingData que representa o instantâneo do sistema virtual que é o instantâneo mais atual em uma ramificação de instantâneos dependentes.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Classe Msvm_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753289"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="45ceb-103">\_Classe Msvm MostCurrentSnapshotInBranch</span><span class="sxs-lookup"><span data-stu-id="45ceb-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="45ceb-104">Associa uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) ou [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa um sistema virtual, com uma instância da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo do sistema virtual que é o instantâneo mais atual em uma ramificação de instantâneos dependentes.</span><span class="sxs-lookup"><span data-stu-id="45ceb-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="45ceb-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="45ceb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ceb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45ceb-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="45ceb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="45ceb-107">Members</span></span>

<span data-ttu-id="45ceb-108">A classe **Msvm \_ MostCurrentSnapshotInBranch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="45ceb-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="45ceb-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="45ceb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45ceb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="45ceb-110">Properties</span></span>

<span data-ttu-id="45ceb-111">A classe **Msvm \_ MostCurrentSnapshotInBranch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="45ceb-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45ceb-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="45ceb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ceb-113">Tipo de dados: **[ **\_ sistema de ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="45ceb-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="45ceb-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45ceb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45ceb-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="45ceb-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="45ceb-116">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) ou [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="45ceb-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="45ceb-117">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="45ceb-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="45ceb-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="45ceb-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ceb-119">Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="45ceb-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="45ceb-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45ceb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45ceb-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="45ceb-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="45ceb-122">Uma referência a uma instância da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo do sistema virtual que é o instantâneo mais atual em uma ramificação de instantâneos dependentes.</span><span class="sxs-lookup"><span data-stu-id="45ceb-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="45ceb-123">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="45ceb-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45ceb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45ceb-124">Requirements</span></span>



| <span data-ttu-id="45ceb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45ceb-125">Requirement</span></span> | <span data-ttu-id="45ceb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="45ceb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ceb-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45ceb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45ceb-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="45ceb-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45ceb-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45ceb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45ceb-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="45ceb-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45ceb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="45ceb-131">Namespace</span></span><br/>                | <span data-ttu-id="45ceb-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="45ceb-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45ceb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="45ceb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45ceb-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45ceb-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45ceb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="45ceb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45ceb-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45ceb-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

