---
description: Uma associação entre uma instância da classe Msvm \_ EthernetSwitchPort e uma instância da \_ classe Msvm EthernetPortData que representa os dados coletados sobre a porta por uma extensão de comutador.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Classe Msvm_EthernetPortInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759243"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="89afb-103">\_Classe Msvm EthernetPortInfo</span><span class="sxs-lookup"><span data-stu-id="89afb-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="89afb-104">Uma associação entre uma instância da classe [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) e uma instância da classe [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) que representa os dados coletados sobre a porta por uma extensão de comutador.</span><span class="sxs-lookup"><span data-stu-id="89afb-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="89afb-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="89afb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89afb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89afb-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="89afb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="89afb-107">Members</span></span>

<span data-ttu-id="89afb-108">A classe **Msvm \_ EthernetPortInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89afb-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="89afb-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89afb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89afb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89afb-110">Properties</span></span>

<span data-ttu-id="89afb-111">A classe **Msvm \_ EthernetPortInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89afb-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89afb-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="89afb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89afb-113">Tipo de dados: **Msvm \_ EthernetSwitchPort**</span><span class="sxs-lookup"><span data-stu-id="89afb-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="89afb-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89afb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89afb-115">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="89afb-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="89afb-116">Uma instância da classe [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa a porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="89afb-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="89afb-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="89afb-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89afb-118">Tipo de dados: **Msvm \_ EthernetPortData**</span><span class="sxs-lookup"><span data-stu-id="89afb-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="89afb-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89afb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89afb-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")</span><span class="sxs-lookup"><span data-stu-id="89afb-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="89afb-121">Uma instância da classe [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) que representa os dados da porta.</span><span class="sxs-lookup"><span data-stu-id="89afb-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89afb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89afb-122">Requirements</span></span>



| <span data-ttu-id="89afb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89afb-123">Requirement</span></span> | <span data-ttu-id="89afb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="89afb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89afb-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89afb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89afb-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89afb-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="89afb-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89afb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89afb-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="89afb-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89afb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="89afb-129">Namespace</span></span><br/>                | <span data-ttu-id="89afb-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="89afb-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89afb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="89afb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89afb-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89afb-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89afb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="89afb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89afb-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89afb-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

