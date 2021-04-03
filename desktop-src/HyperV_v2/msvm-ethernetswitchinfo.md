---
description: Define a associação entre um comutador Ethernet e um recurso de comutador.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Classe Msvm_EthernetSwitchInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922994"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="f1137-103">\_Classe Msvm EthernetSwitchInfo</span><span class="sxs-lookup"><span data-stu-id="f1137-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="f1137-104">Define a associação entre um comutador Ethernet e um recurso de comutador.</span><span class="sxs-lookup"><span data-stu-id="f1137-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="f1137-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f1137-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1137-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1137-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f1137-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f1137-107">Members</span></span>

<span data-ttu-id="f1137-108">A classe **Msvm \_ EthernetSwitchInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1137-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="f1137-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1137-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1137-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1137-110">Properties</span></span>

<span data-ttu-id="f1137-111">A classe **Msvm \_ EthernetSwitchInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1137-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1137-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f1137-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1137-113">Tipo de dados: **Msvm \_ VirtualEthernetSwitch**</span><span class="sxs-lookup"><span data-stu-id="f1137-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="f1137-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1137-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1137-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f1137-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f1137-116">Uma referência à classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="f1137-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="f1137-117">Essa propriedade é derivada da [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f1137-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="f1137-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f1137-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1137-119">Tipo de dados: **Msvm \_ EthernetSwitchData**</span><span class="sxs-lookup"><span data-stu-id="f1137-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="f1137-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1137-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1137-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="f1137-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f1137-122">Uma referência à classe [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md) que representa o recurso de opção.</span><span class="sxs-lookup"><span data-stu-id="f1137-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="f1137-123">Essa propriedade é derivada da [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f1137-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1137-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1137-124">Requirements</span></span>



| <span data-ttu-id="f1137-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1137-125">Requirement</span></span> | <span data-ttu-id="f1137-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f1137-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1137-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1137-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1137-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f1137-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1137-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1137-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1137-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f1137-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1137-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1137-131">Namespace</span></span><br/>                | <span data-ttu-id="f1137-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f1137-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1137-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f1137-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1137-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1137-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1137-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f1137-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1137-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1137-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

