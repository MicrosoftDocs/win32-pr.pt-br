---
description: Representa uma associação entre um serviço e o sistema que hospeda o serviço. Um sistema pode hospedar muitos serviços, no entanto, essa classe não representa serviços hospedados em vários sistemas.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: Classe CIM_HostedService (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457246"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="aace3-104">Classe CIM_HostedService (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="aace3-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="aace3-105">Representa uma associação entre um serviço e o sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="aace3-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="aace3-106">Um sistema pode hospedar muitos serviços, no entanto, essa classe não representa serviços hospedados em vários sistemas.</span><span class="sxs-lookup"><span data-stu-id="aace3-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="aace3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aace3-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="aace3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="aace3-108">Members</span></span>

<span data-ttu-id="aace3-109">A classe **CIM \_ HostedService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aace3-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="aace3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aace3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aace3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aace3-111">Properties</span></span>

<span data-ttu-id="aace3-112">A classe **CIM \_ HostedService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aace3-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aace3-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="aace3-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aace3-114">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="aace3-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="aace3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aace3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aace3-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="aace3-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="aace3-117">O sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="aace3-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="aace3-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="aace3-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aace3-119">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="aace3-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="aace3-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aace3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aace3-121">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aace3-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aace3-122">O serviço hospedado no sistema.</span><span class="sxs-lookup"><span data-stu-id="aace3-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aace3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aace3-123">Requirements</span></span>



| <span data-ttu-id="aace3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aace3-124">Requirement</span></span> | <span data-ttu-id="aace3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="aace3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aace3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aace3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aace3-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aace3-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="aace3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aace3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aace3-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aace3-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="aace3-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="aace3-130">Namespace</span></span><br/>                | <span data-ttu-id="aace3-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="aace3-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aace3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="aace3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aace3-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aace3-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aace3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="aace3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aace3-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aace3-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aace3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="aace3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aace3-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="aace3-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

