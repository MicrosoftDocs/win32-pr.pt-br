---
description: Representa o valor da instância de uma métrica definida por uma instância de CIM \_ AggregationMetricDefinition.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Classe CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758992"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="ea543-103">\_Classe CIM AggregationMetricValue</span><span class="sxs-lookup"><span data-stu-id="ea543-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="ea543-104">Representa o valor da instância de uma métrica definida por uma instância de **CIM \_ AggregationMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="ea543-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea543-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea543-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="ea543-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ea543-106">Members</span></span>

<span data-ttu-id="ea543-107">A classe **CIM \_ AggregationMetricValue** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ea543-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="ea543-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea543-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea543-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea543-109">Properties</span></span>

<span data-ttu-id="ea543-110">A classe **CIM \_ AggregationMetricValue** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea543-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea543-111">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="ea543-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea543-112">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea543-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea543-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea543-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea543-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="ea543-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="ea543-115">Representa a duração da hora em que a agregação foi computada.</span><span class="sxs-lookup"><span data-stu-id="ea543-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="ea543-116">O início de um intervalo de monitoramento sobre o qual a função de agregação é aplicada é determinado pela subtração do valor **AggregationDuration** do valor **AggregationTimestamp** .</span><span class="sxs-lookup"><span data-stu-id="ea543-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="ea543-117">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="ea543-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea543-118">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea543-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea543-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea543-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea543-120">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Duração**")</span><span class="sxs-lookup"><span data-stu-id="ea543-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="ea543-121">A hora em que a função de agregação foi aplicada para determinar o valor da instância de métrica.</span><span class="sxs-lookup"><span data-stu-id="ea543-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="ea543-122">Isso é diferente da hora em que a instância é criada.</span><span class="sxs-lookup"><span data-stu-id="ea543-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="ea543-123">O valor **AggregationTimeStamp** é alterado sempre que a função de agregação é aplicada para calcular o valor.</span><span class="sxs-lookup"><span data-stu-id="ea543-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea543-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea543-124">Requirements</span></span>



| <span data-ttu-id="ea543-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea543-125">Requirement</span></span> | <span data-ttu-id="ea543-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ea543-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea543-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea543-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ea543-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ea543-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ea543-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea543-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ea543-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea543-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ea543-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea543-131">Namespace</span></span><br/>                | <span data-ttu-id="ea543-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ea543-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ea543-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ea543-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea543-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea543-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea543-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ea543-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea543-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea543-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea543-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea543-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea543-138">**\_BASEMETRICVALUE CIM**</span><span class="sxs-lookup"><span data-stu-id="ea543-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 

