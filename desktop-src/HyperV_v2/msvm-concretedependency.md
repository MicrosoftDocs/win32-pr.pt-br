---
description: Define a associação entre uma extensão de comutador Ethernet instalada e uma extensão de comutador Ethernet.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Classe Msvm_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165252"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="06883-103">\_Classe Msvm ConcreteDependency</span><span class="sxs-lookup"><span data-stu-id="06883-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="06883-104">Define a associação entre uma extensão de comutador Ethernet instalada e uma extensão de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="06883-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="06883-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="06883-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06883-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06883-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="06883-107">Membros</span><span class="sxs-lookup"><span data-stu-id="06883-107">Members</span></span>

<span data-ttu-id="06883-108">A classe **Msvm \_ ConcreteDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="06883-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="06883-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06883-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06883-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06883-110">Properties</span></span>

<span data-ttu-id="06883-111">A classe **Msvm \_ ConcreteDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="06883-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06883-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="06883-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06883-113">Tipo de dados: **[ **Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="06883-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="06883-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06883-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06883-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="06883-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="06883-116">Uma referência a uma instância da classe [**Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) que representa um componente de extensão do comutador Ethernet virtual instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="06883-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="06883-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="06883-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06883-118">Tipo de dados: **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="06883-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="06883-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06883-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06883-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="06883-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="06883-121">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa a ocorrência do **Antecedent** associado a um comutador Ethernet virtual específico.</span><span class="sxs-lookup"><span data-stu-id="06883-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06883-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06883-122">Requirements</span></span>



| <span data-ttu-id="06883-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="06883-123">Requirement</span></span> | <span data-ttu-id="06883-124">Valor</span><span class="sxs-lookup"><span data-stu-id="06883-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06883-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06883-125">Minimum supported client</span></span><br/> | <span data-ttu-id="06883-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="06883-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06883-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06883-127">Minimum supported server</span></span><br/> | <span data-ttu-id="06883-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="06883-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06883-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="06883-129">Namespace</span></span><br/>                | <span data-ttu-id="06883-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="06883-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06883-131">MOF</span><span class="sxs-lookup"><span data-stu-id="06883-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06883-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06883-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06883-133">DLL</span><span class="sxs-lookup"><span data-stu-id="06883-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06883-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06883-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

