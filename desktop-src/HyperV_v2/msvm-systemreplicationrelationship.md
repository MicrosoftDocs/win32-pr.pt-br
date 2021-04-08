---
description: Representa uma associação entre uma instância do Msvm \_ ComputerSystem que representa a máquina virtual e uma instância de Msvm \_ ReplicationRelationship que representa um relacionamento de replicação da máquina virtual.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Classe Msvm_SystemReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920725"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="bc7fa-103">\_Classe Msvm SystemReplicationRelationship</span><span class="sxs-lookup"><span data-stu-id="bc7fa-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="bc7fa-104">Representa uma associação entre uma instância do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual e uma instância de [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa um relacionamento de replicação da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc7fa-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="bc7fa-105">Essa classe deriva da classe de [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="bc7fa-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="bc7fa-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bc7fa-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7fa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc7fa-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bc7fa-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bc7fa-108">Members</span></span>

<span data-ttu-id="bc7fa-109">A classe **Msvm \_ SystemReplicationRelationship** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bc7fa-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="bc7fa-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc7fa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc7fa-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc7fa-111">Properties</span></span>

<span data-ttu-id="bc7fa-112">A classe **Msvm \_ SystemReplicationRelationship** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bc7fa-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc7fa-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="bc7fa-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7fa-114">Tipo de dados: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="bc7fa-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bc7fa-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc7fa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7fa-116">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="bc7fa-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bc7fa-117">Referência à instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc7fa-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="bc7fa-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="bc7fa-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7fa-119">Tipo de dados: **Msvm \_ ReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="bc7fa-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="bc7fa-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc7fa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7fa-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")</span><span class="sxs-lookup"><span data-stu-id="bc7fa-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bc7fa-122">Referência à instância da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa a relação de replicação de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="bc7fa-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc7fa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc7fa-123">Requirements</span></span>



| <span data-ttu-id="bc7fa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc7fa-124">Requirement</span></span> | <span data-ttu-id="bc7fa-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bc7fa-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7fa-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc7fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bc7fa-127">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc7fa-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bc7fa-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc7fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bc7fa-129">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="bc7fa-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc7fa-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc7fa-130">Namespace</span></span><br/>                | <span data-ttu-id="bc7fa-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bc7fa-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bc7fa-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bc7fa-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc7fa-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc7fa-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc7fa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bc7fa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc7fa-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc7fa-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc7fa-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc7fa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc7fa-137">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="bc7fa-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="bc7fa-138">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="bc7fa-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

