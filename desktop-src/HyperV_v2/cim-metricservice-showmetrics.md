---
description: 'Relata o seguinte: as métricas disponíveis para serem coletadas para um elemento gerenciado, os elementos gerenciados para os quais uma métrica definida por uma instância do CIM \_ BaseMetricDefinition está disponível para ser coletada e se uma métrica específica está sendo coletada ou não para um elemento gerenciado.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Método de permétricas da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091670"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="1731b-103">Método de permétricas da \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="1731b-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="1731b-104">Relata o seguinte: as métricas disponíveis para serem coletadas para um elemento gerenciado, os elementos gerenciados para os quais uma métrica definida por uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) está disponível para ser coletada e se uma métrica específica está sendo coletada ou não para um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1731b-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="1731b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1731b-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="1731b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1731b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1731b-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1731b-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1731b-108">Identifica uma instância de [**CIM \_ managedelement**](cim-managedelement.md) para a qual o método retorna referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas que estão sendo capturadas para o **CIM \_ managedelement**.</span><span class="sxs-lookup"><span data-stu-id="1731b-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="1731b-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1731b-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1731b-110">Identifica uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="1731b-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="1731b-111">O método retorna referências a instâncias de [**CIM \_ managedelement**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.</span><span class="sxs-lookup"><span data-stu-id="1731b-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="1731b-112">*ManagedElements* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1731b-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1731b-113">Em caso de sucesso, pode conter referências a objetos [**\_ gerenciados CIM**](cim-managedelement.md) para os quais a métrica identificada pelo parâmetro de *definição* está disponível para coleta.</span><span class="sxs-lookup"><span data-stu-id="1731b-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="1731b-114">*Definitionlist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1731b-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1731b-115">Em caso de sucesso, pode conter referências a instâncias de objetos [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) que definem métricas disponíveis para coleta para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="1731b-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1731b-116">*Métricas* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1731b-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1731b-117">Em caso de sucesso, cada índice de matriz deve conter o valor da propriedade **Name** para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .</span><span class="sxs-lookup"><span data-stu-id="1731b-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1731b-118">*MetricCollectionEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1731b-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1731b-119">Indica se uma métrica está sendo coletada para um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1731b-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="1731b-120">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="1731b-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="1731b-121">**Desabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="1731b-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1731b-122">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="1731b-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1731b-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1731b-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1731b-124">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1731b-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="1731b-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1731b-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1731b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1731b-126">Return value</span></span>

<span data-ttu-id="1731b-127">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1731b-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1731b-128">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="1731b-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1731b-129">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="1731b-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1731b-130">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="1731b-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1731b-131">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1731b-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1731b-132">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1731b-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1731b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1731b-133">Requirements</span></span>



| <span data-ttu-id="1731b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1731b-134">Requirement</span></span> | <span data-ttu-id="1731b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1731b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1731b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1731b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1731b-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1731b-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1731b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1731b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1731b-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1731b-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1731b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="1731b-140">Namespace</span></span><br/>                | <span data-ttu-id="1731b-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1731b-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1731b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1731b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1731b-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1731b-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1731b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1731b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1731b-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1731b-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1731b-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1731b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1731b-147">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1731b-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




