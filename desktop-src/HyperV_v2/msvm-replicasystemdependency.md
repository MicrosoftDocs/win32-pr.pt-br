---
description: Representa uma associação entre uma instância da classe de \_ ComputerSystem do CIM que representa a réplica da máquina virtual e uma instância da \_ classe de COMPUTERSYSTEM do CIM que representa a réplica da máquina virtual de teste.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Classe Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169730"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="7fa54-103">\_Classe Msvm ReplicaSystemDependency</span><span class="sxs-lookup"><span data-stu-id="7fa54-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="7fa54-104">Representa uma associação entre uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a réplica da máquina virtual e uma instância da classe de **\_ ComputerSystem do CIM** que representa a réplica da máquina virtual de teste.</span><span class="sxs-lookup"><span data-stu-id="7fa54-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="7fa54-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7fa54-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa54-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fa54-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7fa54-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7fa54-107">Members</span></span>

<span data-ttu-id="7fa54-108">A classe **Msvm \_ ReplicaSystemDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7fa54-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="7fa54-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7fa54-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fa54-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7fa54-110">Properties</span></span>

<span data-ttu-id="7fa54-111">A classe **Msvm \_ ReplicaSystemDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7fa54-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fa54-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="7fa54-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-113">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="7fa54-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa54-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-115">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7fa54-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-116">Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a réplica da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7fa54-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="7fa54-117">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7fa54-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="7fa54-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-119">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="7fa54-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa54-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")</span><span class="sxs-lookup"><span data-stu-id="7fa54-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-122">Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a réplica da máquina virtual de teste criada pelo método [**Msvm \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa54-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="7fa54-123">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7fa54-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fa54-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa54-124">Requirements</span></span>



| <span data-ttu-id="7fa54-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa54-125">Requirement</span></span> | <span data-ttu-id="7fa54-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa54-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa54-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fa54-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa54-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7fa54-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7fa54-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fa54-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa54-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7fa54-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fa54-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fa54-131">Namespace</span></span><br/>                | <span data-ttu-id="7fa54-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7fa54-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7fa54-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7fa54-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fa54-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fa54-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fa54-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7fa54-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fa54-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fa54-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

