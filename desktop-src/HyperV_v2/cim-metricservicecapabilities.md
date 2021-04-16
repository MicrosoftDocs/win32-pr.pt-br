---
description: Descreve os recursos de um \_ objeto CIM MetricService.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: Classe CIM_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759414"
---
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="52da9-103">\_Classe CIM MetricServiceCapabilities</span><span class="sxs-lookup"><span data-stu-id="52da9-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="52da9-104">Descreve os recursos de um objeto [**CIM \_ MetricService**](cim-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="52da9-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="52da9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52da9-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="52da9-106">Membros</span><span class="sxs-lookup"><span data-stu-id="52da9-106">Members</span></span>

<span data-ttu-id="52da9-107">A classe **CIM \_ MetricServiceCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="52da9-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="52da9-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52da9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52da9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52da9-109">Properties</span></span>

<span data-ttu-id="52da9-110">A classe **CIM \_ MetricServiceCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="52da9-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52da9-111">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="52da9-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52da9-112">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52da9-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52da9-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52da9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52da9-114">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**ManagedElementControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="52da9-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="52da9-115">Uma matriz que contém identificadores das instâncias [**\_ gerenciadas CIM**](cim-managedelement.md) que são controladas pelo serviço de métrica.</span><span class="sxs-lookup"><span data-stu-id="52da9-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="52da9-116">Os identificadores devem ser formatados como URIs WBEM (Web-Based Enterprise Management).</span><span class="sxs-lookup"><span data-stu-id="52da9-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="52da9-117">Para usar essa propriedade, o serviço de métrica deve dar suporte à habilitação ou desabilitação de pelo menos uma métrica que é definida para a instância de **\_ managedelement CIM** .</span><span class="sxs-lookup"><span data-stu-id="52da9-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="52da9-118">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="52da9-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52da9-119">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52da9-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52da9-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52da9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52da9-121">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**MetricControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="52da9-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="52da9-122">Uma matriz que contém identificadores do [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que define as métricas que são gerenciadas pelo serviço de métrica.</span><span class="sxs-lookup"><span data-stu-id="52da9-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="52da9-123">Os identificadores devem ser formatados como URIs WBEM (Web-Based Enterprise Management).</span><span class="sxs-lookup"><span data-stu-id="52da9-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="52da9-124">Para usar essa propriedade, uma instância de [**\_ BaseMetricDefinition do CIM**](cim-basemetricdefinition.md) deve ser associada a uma instância de [**\_ MetricService do CIM**](cim-metricservice.md) por meio da classe [**CIM \_ imafetable**](cim-serviceaffectselement.md) .</span><span class="sxs-lookup"><span data-stu-id="52da9-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="52da9-125">Além disso, o serviço de métrica deve dar suporte à habilitação ou desabilitação de pelo menos uma métrica que é definida pela instância **\_ BaseMetricDefinition do CIM** .</span><span class="sxs-lookup"><span data-stu-id="52da9-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="52da9-126">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="52da9-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52da9-127">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52da9-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52da9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52da9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52da9-129">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**ControllableManagedElements**")</span><span class="sxs-lookup"><span data-stu-id="52da9-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="52da9-130">Uma matriz que indica os tipos de controle que são suportados pelo serviço de métrica para os elementos gerenciados na matriz **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="52da9-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="52da9-131">Essa matriz corresponde à matriz **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="52da9-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="52da9-132">Os tipos de controle nessa matriz são associados às métricas por meio da matriz **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="52da9-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52da9-133">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="52da9-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="52da9-134">**Discreto** (2)</span><span class="sxs-lookup"><span data-stu-id="52da9-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="52da9-135">**Em massa** (3)</span><span class="sxs-lookup"><span data-stu-id="52da9-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="52da9-136">**Ambos** (4)</span><span class="sxs-lookup"><span data-stu-id="52da9-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="52da9-137">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="52da9-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="52da9-138">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="52da9-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52da9-139">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="52da9-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52da9-140">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52da9-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52da9-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52da9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52da9-142">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**ControllableMetrics**")</span><span class="sxs-lookup"><span data-stu-id="52da9-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="52da9-143">Uma matriz que indica os tipos de controle que são suportados pelo serviço de métrica.</span><span class="sxs-lookup"><span data-stu-id="52da9-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="52da9-144">Essa matriz corresponde à matriz **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="52da9-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="52da9-145">Os tipos de controle nessa matriz são associados às métricas por meio da matriz **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="52da9-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52da9-146">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="52da9-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="52da9-147">**Discreto** (2)</span><span class="sxs-lookup"><span data-stu-id="52da9-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="52da9-148">**Em massa** (3)</span><span class="sxs-lookup"><span data-stu-id="52da9-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="52da9-149">**Ambos** (4)</span><span class="sxs-lookup"><span data-stu-id="52da9-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="52da9-150">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="52da9-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="52da9-151">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="52da9-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52da9-152">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="52da9-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52da9-153">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52da9-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52da9-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52da9-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52da9-155">Uma matriz que contém nomes de métodos aos quais o serviço de métrica dá suporte.</span><span class="sxs-lookup"><span data-stu-id="52da9-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="52da9-156">**ControlMetrics** (2)</span><span class="sxs-lookup"><span data-stu-id="52da9-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="52da9-157">**ControlMetricsByClass** (3)</span><span class="sxs-lookup"><span data-stu-id="52da9-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="52da9-158">**Permétricas** (4)</span><span class="sxs-lookup"><span data-stu-id="52da9-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="52da9-159">**ShowMetricsByClass** (5)</span><span class="sxs-lookup"><span data-stu-id="52da9-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="52da9-160">**GetMetricValues** (6)</span><span class="sxs-lookup"><span data-stu-id="52da9-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="52da9-161">**ControlSampleTimes** (7)</span><span class="sxs-lookup"><span data-stu-id="52da9-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="52da9-162">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="52da9-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="52da9-163">**Específico do fornecedor** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="52da9-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="52da9-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="52da9-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="52da9-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52da9-165">Requirements</span></span>



| <span data-ttu-id="52da9-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="52da9-166">Requirement</span></span> | <span data-ttu-id="52da9-167">Valor</span><span class="sxs-lookup"><span data-stu-id="52da9-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52da9-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52da9-168">Minimum supported client</span></span><br/> | <span data-ttu-id="52da9-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52da9-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="52da9-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52da9-170">Minimum supported server</span></span><br/> | <span data-ttu-id="52da9-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52da9-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="52da9-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="52da9-172">Namespace</span></span><br/>                | <span data-ttu-id="52da9-173">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="52da9-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="52da9-174">MOF</span><span class="sxs-lookup"><span data-stu-id="52da9-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52da9-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52da9-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52da9-176">DLL</span><span class="sxs-lookup"><span data-stu-id="52da9-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52da9-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52da9-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="52da9-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="52da9-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52da9-179">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="52da9-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

