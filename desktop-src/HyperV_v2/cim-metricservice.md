---
description: Gerencia métricas para elementos gerenciados.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757153"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="e33b4-103">\_Classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="e33b4-103">CIM\_MetricService class</span></span>

<span data-ttu-id="e33b4-104">Gerencia métricas para elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e33b4-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e33b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e33b4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="e33b4-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e33b4-106">Members</span></span>

<span data-ttu-id="e33b4-107">A classe **CIM \_ MetricService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e33b4-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="e33b4-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e33b4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e33b4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e33b4-109">Methods</span></span>

<span data-ttu-id="e33b4-110">A classe **CIM \_ MetricService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e33b4-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="e33b4-111">Método</span><span class="sxs-lookup"><span data-stu-id="e33b4-111">Method</span></span>                                                                   | <span data-ttu-id="e33b4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e33b4-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e33b4-113">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="e33b4-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="e33b4-114">Habilita e desabilita a coleção de métricas.</span><span class="sxs-lookup"><span data-stu-id="e33b4-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="e33b4-115">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="e33b4-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="e33b4-116">Habilita e desabilita a coleção de métricas para uma classe.</span><span class="sxs-lookup"><span data-stu-id="e33b4-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e33b4-117">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="e33b4-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="e33b4-118">Especifica quando as métricas são coletadas.</span><span class="sxs-lookup"><span data-stu-id="e33b4-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="e33b4-119">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="e33b4-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="e33b4-120">Recupera uma lista filtrada de valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="e33b4-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="e33b4-121">**Permétricas**</span><span class="sxs-lookup"><span data-stu-id="e33b4-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="e33b4-122">Indica se a coleta de métrica está habilitada para os elementos gerenciados especificados e indica as métricas que estão disponíveis para coleta para cada elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e33b4-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="e33b4-123">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="e33b4-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="e33b4-124">Indica quais métricas estão disponíveis para coleta para todas as instâncias de uma classe CIM.</span><span class="sxs-lookup"><span data-stu-id="e33b4-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="e33b4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e33b4-125">Requirements</span></span>



| <span data-ttu-id="e33b4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e33b4-126">Requirement</span></span> | <span data-ttu-id="e33b4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e33b4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e33b4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e33b4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e33b4-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e33b4-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e33b4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e33b4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e33b4-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e33b4-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e33b4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e33b4-132">Namespace</span></span><br/>                | <span data-ttu-id="e33b4-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e33b4-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e33b4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e33b4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e33b4-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e33b4-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e33b4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e33b4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e33b4-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e33b4-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e33b4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e33b4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e33b4-139">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="e33b4-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




