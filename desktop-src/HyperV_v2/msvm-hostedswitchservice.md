---
description: Uma associação que conecta um serviço de comutador virtual a um serviço de ponte transparente.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Classe Msvm_HostedSwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778749"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="aac3c-103">\_Classe Msvm HostedSwitchService</span><span class="sxs-lookup"><span data-stu-id="aac3c-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="aac3c-104">Uma associação que conecta um serviço de comutador virtual a um serviço de ponte transparente.</span><span class="sxs-lookup"><span data-stu-id="aac3c-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="aac3c-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="aac3c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac3c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aac3c-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="aac3c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="aac3c-107">Members</span></span>

<span data-ttu-id="aac3c-108">A classe **Msvm \_ HostedSwitchService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aac3c-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="aac3c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aac3c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aac3c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aac3c-110">Properties</span></span>

<span data-ttu-id="aac3c-111">A classe **Msvm \_ HostedSwitchService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aac3c-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aac3c-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="aac3c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac3c-113">Tipo de dados: **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="aac3c-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="aac3c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aac3c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac3c-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="aac3c-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aac3c-116">Uma referência a uma instância da classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="aac3c-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="aac3c-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="aac3c-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac3c-118">Tipo de dados: **[ **\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="aac3c-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="aac3c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aac3c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aac3c-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="aac3c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aac3c-121">Uma referência a uma instância da classe [**Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa o serviço de ponte.</span><span class="sxs-lookup"><span data-stu-id="aac3c-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aac3c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="aac3c-122">Remarks</span></span>

<span data-ttu-id="aac3c-123">O acesso à classe **Msvm \_ HostedSwitchService** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="aac3c-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="aac3c-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="aac3c-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="aac3c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aac3c-125">Requirements</span></span>



| <span data-ttu-id="aac3c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aac3c-126">Requirement</span></span> | <span data-ttu-id="aac3c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="aac3c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac3c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aac3c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aac3c-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="aac3c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aac3c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aac3c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aac3c-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="aac3c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aac3c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="aac3c-132">Namespace</span></span><br/>                | <span data-ttu-id="aac3c-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="aac3c-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aac3c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="aac3c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aac3c-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aac3c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aac3c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="aac3c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aac3c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aac3c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aac3c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="aac3c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac3c-139">**HostedService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="aac3c-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="aac3c-140">**HostedService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="aac3c-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

