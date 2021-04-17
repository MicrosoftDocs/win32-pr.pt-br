---
description: Associa um serviço ao seu sistema de computador de hospedagem.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Classe Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782808"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="5d6a9-103">\_Classe Msvm HostedService</span><span class="sxs-lookup"><span data-stu-id="5d6a9-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="5d6a9-104">Associa um serviço ao seu sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="5d6a9-105">As instâncias de [**Msvm \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) podem ser descobertas por meio de sua associação com um host.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="5d6a9-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6a9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d6a9-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5d6a9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5d6a9-108">Members</span></span>

<span data-ttu-id="5d6a9-109">A classe **Msvm \_ HostedService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d6a9-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="5d6a9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d6a9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d6a9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d6a9-111">Properties</span></span>

<span data-ttu-id="5d6a9-112">A classe **Msvm \_ HostedService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d6a9-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="5d6a9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6a9-114">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="5d6a9-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="5d6a9-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d6a9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d6a9-116">Uma referência ao sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="5d6a9-117">Essa propriedade é herdada de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="5d6a9-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="5d6a9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6a9-119">Tipo de dados: **[ **\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="5d6a9-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="5d6a9-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d6a9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d6a9-121">Uma referência ao serviço que está sendo hospedado.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-121">A reference to the service being hosted.</span></span> <span data-ttu-id="5d6a9-122">Essa propriedade é herdada de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d6a9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d6a9-123">Remarks</span></span>

<span data-ttu-id="5d6a9-124">O acesso à classe **Msvm \_ HostedService** pode ser restringido pela filtragem UAC.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5d6a9-125">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="5d6a9-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d6a9-126">Examples</span></span>

<span data-ttu-id="5d6a9-127">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d6a9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d6a9-128">Requirements</span></span>



| <span data-ttu-id="5d6a9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d6a9-129">Requirement</span></span> | <span data-ttu-id="5d6a9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5d6a9-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6a9-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d6a9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5d6a9-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5d6a9-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d6a9-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d6a9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5d6a9-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5d6a9-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d6a9-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d6a9-135">Namespace</span></span><br/>                | <span data-ttu-id="5d6a9-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5d6a9-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5d6a9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5d6a9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d6a9-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d6a9-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d6a9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5d6a9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d6a9-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d6a9-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d6a9-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d6a9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6a9-142">**HostedService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5d6a9-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="5d6a9-143">**HostedService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5d6a9-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="5d6a9-144">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="5d6a9-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

