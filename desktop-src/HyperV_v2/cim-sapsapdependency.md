---
description: Representa uma associação entre dois pontos de acesso de serviço (SAP), em que um SAP depende do outro para utilizar ou se conectar a um serviço.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: Classe CIM_SAPSAPDependency (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501898"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="1191a-103">Classe CIM_SAPSAPDependency (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="1191a-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="1191a-104">Representa uma associação entre dois pontos de acesso de serviço (SAP), em que um SAP depende do outro para utilizar ou se conectar a um serviço.</span><span class="sxs-lookup"><span data-stu-id="1191a-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="1191a-105">Por exemplo, para imprimir em uma impressora de rede, os pontos de acesso de impressão local devem utilizar SAPs subjacentes relacionados à rede para enviar a solicitação de impressão.</span><span class="sxs-lookup"><span data-stu-id="1191a-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1191a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1191a-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1191a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1191a-107">Members</span></span>

<span data-ttu-id="1191a-108">A classe **CIM \_ SAPSAPDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1191a-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="1191a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1191a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1191a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1191a-110">Properties</span></span>

<span data-ttu-id="1191a-111">A classe **CIM \_ SAPSAPDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1191a-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1191a-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1191a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1191a-113">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="1191a-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="1191a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1191a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1191a-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1191a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1191a-116">Uma referência para o SAP necessário.</span><span class="sxs-lookup"><span data-stu-id="1191a-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="1191a-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1191a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1191a-118">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="1191a-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="1191a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1191a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1191a-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="1191a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1191a-121">Uma referência ao SAP dependente.</span><span class="sxs-lookup"><span data-stu-id="1191a-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1191a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1191a-122">Requirements</span></span>



| <span data-ttu-id="1191a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1191a-123">Requirement</span></span> | <span data-ttu-id="1191a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1191a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1191a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1191a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1191a-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1191a-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1191a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1191a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1191a-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1191a-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1191a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1191a-129">Namespace</span></span><br/>                | <span data-ttu-id="1191a-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1191a-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1191a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1191a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1191a-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1191a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1191a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1191a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1191a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1191a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1191a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1191a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1191a-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1191a-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

