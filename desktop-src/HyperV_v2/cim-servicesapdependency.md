---
description: Representa uma associação entre um serviço e um ponto de acesso de serviço (SAP) que fornece a funcionalidade do serviço.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: Classe CIM_ServiceSAPDependency (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756934"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="0edac-103">Classe CIM_ServiceSAPDependency (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0edac-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="0edac-104">Representa uma associação entre um serviço e um ponto de acesso de serviço (SAP) que fornece a funcionalidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="0edac-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0edac-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0edac-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0edac-106">Members</span></span>

<span data-ttu-id="0edac-107">A classe **CIM \_ ServiceSAPDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0edac-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0edac-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0edac-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0edac-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0edac-109">Properties</span></span>

<span data-ttu-id="0edac-110">A classe **CIM \_ ServiceSAPDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0edac-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0edac-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="0edac-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edac-112">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="0edac-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="0edac-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0edac-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0edac-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0edac-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0edac-115">O ponto de acesso de serviço necessário.</span><span class="sxs-lookup"><span data-stu-id="0edac-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="0edac-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="0edac-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edac-117">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="0edac-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="0edac-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0edac-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0edac-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="0edac-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0edac-120">O serviço que é dependente do SAP.</span><span class="sxs-lookup"><span data-stu-id="0edac-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0edac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edac-121">Requirements</span></span>



| <span data-ttu-id="0edac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edac-122">Requirement</span></span> | <span data-ttu-id="0edac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0edac-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0edac-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0edac-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0edac-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0edac-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0edac-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0edac-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0edac-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0edac-128">Namespace</span></span><br/>                | <span data-ttu-id="0edac-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0edac-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0edac-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0edac-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0edac-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0edac-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0edac-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0edac-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0edac-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0edac-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0edac-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0edac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0edac-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="0edac-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

