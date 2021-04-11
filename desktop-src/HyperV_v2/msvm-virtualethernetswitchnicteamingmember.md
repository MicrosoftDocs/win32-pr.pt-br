---
description: Representa a associação entre um ExternalEthernetPort de equipe e um ExternalEthernetPort de membro.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Classe Msvm_VirtualEthernetSwitchNicTeamingMember
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172344"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="59c62-103">\_Classe Msvm VirtualEthernetSwitchNicTeamingMember</span><span class="sxs-lookup"><span data-stu-id="59c62-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="59c62-104">Representa a associação entre um ExternalEthernetPort de equipe e um ExternalEthernetPort de membro.</span><span class="sxs-lookup"><span data-stu-id="59c62-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="59c62-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="59c62-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c62-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59c62-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="59c62-107">Membros</span><span class="sxs-lookup"><span data-stu-id="59c62-107">Members</span></span>

<span data-ttu-id="59c62-108">A classe **Msvm \_ VirtualEthernetSwitchNicTeamingMember** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59c62-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="59c62-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59c62-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59c62-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59c62-110">Properties</span></span>

<span data-ttu-id="59c62-111">A classe **Msvm \_ VirtualEthernetSwitchNicTeamingMember** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="59c62-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59c62-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="59c62-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c62-113">Tipo de dados: **Msvm \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="59c62-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="59c62-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59c62-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59c62-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="59c62-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="59c62-116">Um [**\_ ExternalEthernetPort Msvm**](msvm-externalethernetport.md) que faz referência à instância de porta Ethernet externa da equipe.</span><span class="sxs-lookup"><span data-stu-id="59c62-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="59c62-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="59c62-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c62-118">Tipo de dados: **Msvm \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="59c62-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="59c62-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59c62-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59c62-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="59c62-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="59c62-121">Referência à instância do membro [**Msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="59c62-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59c62-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c62-122">Requirements</span></span>



| <span data-ttu-id="59c62-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c62-123">Requirement</span></span> | <span data-ttu-id="59c62-124">Valor</span><span class="sxs-lookup"><span data-stu-id="59c62-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c62-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59c62-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="59c62-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="59c62-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59c62-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="59c62-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="59c62-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="59c62-129">Namespace</span></span><br/>                | <span data-ttu-id="59c62-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="59c62-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="59c62-131">MOF</span><span class="sxs-lookup"><span data-stu-id="59c62-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59c62-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59c62-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59c62-133">DLL</span><span class="sxs-lookup"><span data-stu-id="59c62-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c62-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59c62-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59c62-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="59c62-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c62-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="59c62-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

