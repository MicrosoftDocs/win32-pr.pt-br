---
description: Representa uma associação entre uma instância de um valor de métrica e uma definição de métrica.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: Classe CIM_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: defba85f46e037c226a96cfaa8ffac44b99244f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787528"
---
# <a name="cim_metricinstance-class"></a><span data-ttu-id="6c69c-103">\_Classe CIM MetricInstance</span><span class="sxs-lookup"><span data-stu-id="6c69c-103">CIM\_MetricInstance class</span></span>

<span data-ttu-id="6c69c-104">Representa uma associação entre uma instância de um valor de métrica e uma definição de métrica.</span><span class="sxs-lookup"><span data-stu-id="6c69c-104">Represents an association between an instance of a metric value and a metric definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c69c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c69c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6c69c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6c69c-106">Members</span></span>

<span data-ttu-id="6c69c-107">A classe **CIM \_ MetricInstance** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6c69c-107">The **CIM\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="6c69c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c69c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c69c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c69c-109">Properties</span></span>

<span data-ttu-id="6c69c-110">A classe **CIM \_ MetricInstance** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6c69c-110">The **CIM\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c69c-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="6c69c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c69c-112">Tipo de dados: **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="6c69c-112">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="6c69c-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c69c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c69c-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6c69c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6c69c-115">A definição do valor da métrica.</span><span class="sxs-lookup"><span data-stu-id="6c69c-115">The definition of the metric value.</span></span>

</dd> <dt>

<span data-ttu-id="6c69c-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="6c69c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c69c-117">Tipo de dados: **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="6c69c-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="6c69c-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c69c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c69c-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="6c69c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6c69c-120">O valor da métrica associada à definição da métrica.</span><span class="sxs-lookup"><span data-stu-id="6c69c-120">The metric value that is associated with the metric definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c69c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c69c-121">Requirements</span></span>



| <span data-ttu-id="6c69c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c69c-122">Requirement</span></span> | <span data-ttu-id="6c69c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6c69c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c69c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c69c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c69c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6c69c-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6c69c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c69c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c69c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c69c-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6c69c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c69c-128">Namespace</span></span><br/>                | <span data-ttu-id="6c69c-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6c69c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c69c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6c69c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c69c-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c69c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6c69c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c69c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c69c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c69c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c69c-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="6c69c-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

