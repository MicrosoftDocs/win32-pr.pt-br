---
description: Representa uma associação entre um ponto de acesso de serviço (SAP) e o sistema que o hospeda.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: Classe CIM_HostedAccessPoint (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457247"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="e265d-103">Classe CIM_HostedAccessPoint (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e265d-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="e265d-104">Representa uma associação entre um ponto de acesso de serviço (SAP) e o sistema que o hospeda.</span><span class="sxs-lookup"><span data-stu-id="e265d-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="e265d-105">Um sistema pode hospedar vários pontos de acesso.</span><span class="sxs-lookup"><span data-stu-id="e265d-105">A system can host multiple access points.</span></span> <span data-ttu-id="e265d-106">Se a implementação do SAP for modelada, ela deverá ser implementada por um recurso de dispositivo ou software que faz parte do sistema que hospeda o SAP.</span><span class="sxs-lookup"><span data-stu-id="e265d-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="e265d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e265d-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e265d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e265d-108">Members</span></span>

<span data-ttu-id="e265d-109">A classe **CIM \_ HostedAccessPoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e265d-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e265d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e265d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e265d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e265d-111">Properties</span></span>

<span data-ttu-id="e265d-112">A classe **CIM \_ HostedAccessPoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e265d-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e265d-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e265d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e265d-114">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="e265d-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="e265d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e265d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e265d-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e265d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e265d-117">O sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="e265d-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="e265d-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e265d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e265d-119">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="e265d-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="e265d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e265d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e265d-121">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e265d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e265d-122">Os SAPs hospedados no sistema.</span><span class="sxs-lookup"><span data-stu-id="e265d-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e265d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e265d-123">Requirements</span></span>



| <span data-ttu-id="e265d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e265d-124">Requirement</span></span> | <span data-ttu-id="e265d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e265d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e265d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e265d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e265d-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e265d-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e265d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e265d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e265d-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e265d-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e265d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e265d-130">Namespace</span></span><br/>                | <span data-ttu-id="e265d-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e265d-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e265d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e265d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e265d-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e265d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e265d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e265d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e265d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e265d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e265d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e265d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e265d-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="e265d-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

