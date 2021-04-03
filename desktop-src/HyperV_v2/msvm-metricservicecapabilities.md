---
description: Descreve os recursos da \_ instância Msvm MetricService associada.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Classe Msvm_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837130"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="589ee-103">\_Classe Msvm MetricServiceCapabilities</span><span class="sxs-lookup"><span data-stu-id="589ee-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="589ee-104">Descreve os recursos da instância [**Msvm \_ MetricService**](msvm-metricservice.md) associada.</span><span class="sxs-lookup"><span data-stu-id="589ee-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="589ee-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="589ee-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="589ee-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="589ee-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="589ee-107">Membros</span><span class="sxs-lookup"><span data-stu-id="589ee-107">Members</span></span>

<span data-ttu-id="589ee-108">A classe **Msvm \_ MetricServiceCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="589ee-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="589ee-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="589ee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="589ee-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="589ee-110">Properties</span></span>

<span data-ttu-id="589ee-111">A classe **Msvm \_ MetricServiceCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="589ee-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="589ee-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="589ee-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="589ee-115">A short description of the object.</span></span> <span data-ttu-id="589ee-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos do serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="589ee-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="589ee-117">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="589ee-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-118">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="589ee-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589ee-120">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="589ee-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="589ee-121">Identifica as instâncias de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que podem ser controladas pela instância **\_ MetricService do CIM** associada.</span><span class="sxs-lookup"><span data-stu-id="589ee-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="589ee-122">Se essa propriedade for **nula**, todos os elementos poderão ser controlados.</span><span class="sxs-lookup"><span data-stu-id="589ee-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="589ee-123">Essa propriedade é herdada do **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="589ee-124">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="589ee-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-125">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="589ee-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589ee-127">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="589ee-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="589ee-128">Identifica as instâncias de **\_ BaseMetricDefinition CIM** que podem ser controladas pela instância **\_ MetricService do CIM** associada.</span><span class="sxs-lookup"><span data-stu-id="589ee-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="589ee-129">Se essa propriedade for **nula**, todas as métricas poderão ser controladas.</span><span class="sxs-lookup"><span data-stu-id="589ee-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="589ee-130">Essa propriedade é herdada do **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="589ee-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="589ee-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-134">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="589ee-134">A description of the object.</span></span> <span data-ttu-id="589ee-135">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "define os recursos do serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="589ee-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="589ee-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="589ee-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-139">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="589ee-139">A display name for the object.</span></span> <span data-ttu-id="589ee-140">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos do serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="589ee-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="589ee-141">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="589ee-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="589ee-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-144">Indica se a propriedade **ElementName** pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="589ee-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="589ee-145">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="589ee-146">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="589ee-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-149">Especifica as restrições em **ElementName**, expressas como uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="589ee-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="589ee-150">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="589ee-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="589ee-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="589ee-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589ee-154">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="589ee-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="589ee-155">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="589ee-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="589ee-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="589ee-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="589ee-157">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="589ee-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-158">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="589ee-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="589ee-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589ee-160">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="589ee-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="589ee-161">Identifica o tipo de controle com suporte da instância **\_ MetricService do CIM** associada para o objeto [**CIM \_ gerenciadoelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificado pelo valor no mesmo índice de matriz na propriedade **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="589ee-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="589ee-162">Se essa propriedade for **nula**, todos os tipos de controle serão suportados.</span><span class="sxs-lookup"><span data-stu-id="589ee-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="589ee-163">Essa propriedade é herdada do **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="589ee-164">Valor</span><span class="sxs-lookup"><span data-stu-id="589ee-164">Value</span></span>                                                                                   | <span data-ttu-id="589ee-165">Significado</span><span class="sxs-lookup"><span data-stu-id="589ee-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="589ee-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="589ee-167">Unknown</span><span class="sxs-lookup"><span data-stu-id="589ee-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="589ee-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="589ee-169">Discreto</span><span class="sxs-lookup"><span data-stu-id="589ee-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="589ee-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="589ee-171">Em massa</span><span class="sxs-lookup"><span data-stu-id="589ee-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="589ee-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="589ee-173">Ambos</span><span class="sxs-lookup"><span data-stu-id="589ee-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="589ee-174"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="589ee-175">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="589ee-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="589ee-176"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="589ee-177">Específico do fornecedor</span><span class="sxs-lookup"><span data-stu-id="589ee-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="589ee-178">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="589ee-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-179">Tipo de dados: **unit16**</span><span class="sxs-lookup"><span data-stu-id="589ee-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="589ee-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589ee-181">Qualificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="589ee-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="589ee-182">Especifica o comprimento máximo com suporte da propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="589ee-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="589ee-183">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="589ee-184">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="589ee-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-185">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="589ee-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="589ee-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589ee-187">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="589ee-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="589ee-188">Identifica o tipo de controle suportado pela instância **\_ MetricService do CIM** associada para o **\_ BaseMetricDefinition CIM** identificado pelo valor no mesmo índice de matriz na propriedade **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="589ee-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="589ee-189">Se essa propriedade for **nula**, todos os tipos de controle serão suportados.</span><span class="sxs-lookup"><span data-stu-id="589ee-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="589ee-190">Essa propriedade é herdada do **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="589ee-191">Valor</span><span class="sxs-lookup"><span data-stu-id="589ee-191">Value</span></span>                                                                                   | <span data-ttu-id="589ee-192">Significado</span><span class="sxs-lookup"><span data-stu-id="589ee-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="589ee-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="589ee-194">Unknown</span><span class="sxs-lookup"><span data-stu-id="589ee-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="589ee-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="589ee-196">Discreto</span><span class="sxs-lookup"><span data-stu-id="589ee-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="589ee-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="589ee-198">Em massa</span><span class="sxs-lookup"><span data-stu-id="589ee-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="589ee-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="589ee-200">Ambos</span><span class="sxs-lookup"><span data-stu-id="589ee-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="589ee-201"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="589ee-202">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="589ee-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="589ee-203"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="589ee-204">Específico do fornecedor</span><span class="sxs-lookup"><span data-stu-id="589ee-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="589ee-205">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="589ee-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-206">Tipo de dados: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="589ee-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="589ee-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-208">Indica os possíveis Estados que podem ser solicitados ao usar o método **RequestStateChange** no elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="589ee-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="589ee-209">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="589ee-210">Valor</span><span class="sxs-lookup"><span data-stu-id="589ee-210">Value</span></span>                                                                         | <span data-ttu-id="589ee-211">Significado</span><span class="sxs-lookup"><span data-stu-id="589ee-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="589ee-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="589ee-213">habilitado</span><span class="sxs-lookup"><span data-stu-id="589ee-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="589ee-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="589ee-215">Desabilita</span><span class="sxs-lookup"><span data-stu-id="589ee-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="589ee-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="589ee-217">Desligar</span><span class="sxs-lookup"><span data-stu-id="589ee-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="589ee-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="589ee-219">Offline</span><span class="sxs-lookup"><span data-stu-id="589ee-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="589ee-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="589ee-221">Teste</span><span class="sxs-lookup"><span data-stu-id="589ee-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="589ee-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="589ee-223">Ferida</span><span class="sxs-lookup"><span data-stu-id="589ee-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="589ee-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="589ee-225">Fechar</span><span class="sxs-lookup"><span data-stu-id="589ee-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="589ee-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="589ee-227">Reboot</span><span class="sxs-lookup"><span data-stu-id="589ee-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="589ee-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="589ee-229">Redefinir</span><span class="sxs-lookup"><span data-stu-id="589ee-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="589ee-230">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="589ee-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589ee-231">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="589ee-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="589ee-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="589ee-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="589ee-233">Especifica os métodos com suporte pelo serviço de métrica.</span><span class="sxs-lookup"><span data-stu-id="589ee-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="589ee-234">Essa propriedade é herdada do **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="589ee-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="589ee-235">Valor</span><span class="sxs-lookup"><span data-stu-id="589ee-235">Value</span></span>                                                                                   | <span data-ttu-id="589ee-236">Significado</span><span class="sxs-lookup"><span data-stu-id="589ee-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="589ee-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="589ee-238">Há suporte para o método [**ControlMetrics**](controlmetrics-msvm-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="589ee-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="589ee-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="589ee-240">Há suporte para o método **ControlMetricsByClass** .</span><span class="sxs-lookup"><span data-stu-id="589ee-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="589ee-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="589ee-242">Há suporte para o método não há **métricas** .</span><span class="sxs-lookup"><span data-stu-id="589ee-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="589ee-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="589ee-244">Há suporte para o método **ShowMetricsByClass** .</span><span class="sxs-lookup"><span data-stu-id="589ee-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="589ee-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="589ee-246">Há suporte para o método **GetMetricValues** .</span><span class="sxs-lookup"><span data-stu-id="589ee-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="589ee-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="589ee-248">Há suporte para o método **ControlSampleTimes** .</span><span class="sxs-lookup"><span data-stu-id="589ee-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="589ee-249"><dt>8.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="589ee-250">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="589ee-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="589ee-251"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="589ee-252">Específico do fornecedor</span><span class="sxs-lookup"><span data-stu-id="589ee-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="589ee-253">Requisitos</span><span class="sxs-lookup"><span data-stu-id="589ee-253">Requirements</span></span>



| <span data-ttu-id="589ee-254">Requisito</span><span class="sxs-lookup"><span data-stu-id="589ee-254">Requirement</span></span> | <span data-ttu-id="589ee-255">Valor</span><span class="sxs-lookup"><span data-stu-id="589ee-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589ee-256">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="589ee-256">Minimum supported client</span></span><br/> | <span data-ttu-id="589ee-257">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="589ee-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="589ee-258">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="589ee-258">Minimum supported server</span></span><br/> | <span data-ttu-id="589ee-259">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="589ee-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="589ee-260">Namespace</span><span class="sxs-lookup"><span data-stu-id="589ee-260">Namespace</span></span><br/>                | <span data-ttu-id="589ee-261">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="589ee-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="589ee-262">MOF</span><span class="sxs-lookup"><span data-stu-id="589ee-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="589ee-263"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="589ee-264">DLL</span><span class="sxs-lookup"><span data-stu-id="589ee-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="589ee-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="589ee-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="589ee-266">Confira também</span><span class="sxs-lookup"><span data-stu-id="589ee-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589ee-267">**\_METRICSERVICECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="589ee-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="589ee-268">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="589ee-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

