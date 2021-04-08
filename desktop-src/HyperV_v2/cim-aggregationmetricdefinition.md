---
description: Representa a definição de uma métrica que é derivada de outro valor de métrica. Um \_ objeto CIM AggregationMetricDefinition deve ser associado aos objetos CIM \_ managedelement aos quais ele se aplica.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: Classe CIM_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661868"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="ef0dc-104">\_Classe CIM AggregationMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ef0dc-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="ef0dc-105">Representa a definição de uma métrica que é derivada de outro valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="ef0dc-106">Um objeto **CIM \_ AggregationMetricDefinition** deve ser associado aos objetos **CIM \_ managedelement** aos quais ele se aplica.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0dc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef0dc-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="ef0dc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ef0dc-108">Members</span></span>

<span data-ttu-id="ef0dc-109">A classe **CIM \_ AggregationMetricDefinition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ef0dc-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="ef0dc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ef0dc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef0dc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ef0dc-111">Properties</span></span>

<span data-ttu-id="ef0dc-112">A classe **CIM \_ AggregationMetricDefinition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef0dc-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="ef0dc-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0dc-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0dc-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0dc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0dc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0dc-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("altertype"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricDefinition**.**Iscontinuous**")</span><span class="sxs-lookup"><span data-stu-id="ef0dc-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0dc-117">Indica como o valor da métrica muda usando atributos comuns, como alteração de direção, valores mínimos e máximos e semântica de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="ef0dc-118">**Função simples** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ef0dc-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ef0dc-120">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0dc-121">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="ef0dc-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0dc-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0dc-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0dc-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0dc-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0dc-124">A computação básica executada em uma métrica subjacente para chegar ao valor dessa métrica derivada.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="ef0dc-125">Essa propriedade é **nula** quando a propriedade **altertype** tem um valor diferente de "5" (função simples).</span><span class="sxs-lookup"><span data-stu-id="ef0dc-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ef0dc-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="ef0dc-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ef0dc-128">A métrica relata o menor valor detectado para a entidade monitorada associada.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="ef0dc-129">Isso também é conhecido como marca-d ' água baixa.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="ef0dc-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef0dc-131">A métrica relata o valor máximo detectado para a entidade monitorada associada.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="ef0dc-132">Isso também é conhecido como uma marca d' água alta.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="ef0dc-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Média** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ef0dc-134">A métrica relata o valor médio dos valores de métrica subjacentes.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="ef0dc-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ef0dc-136">A métrica relata o valor mediano dos valores de métrica subjacentes.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="ef0dc-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ef0dc-138">a métrica relata o valor modal dos valores de métrica subjacentes.</span><span class="sxs-lookup"><span data-stu-id="ef0dc-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ef0dc-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ef0dc-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="ef0dc-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ef0dc-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ef0dc-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef0dc-141">Requirements</span></span>



| <span data-ttu-id="ef0dc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0dc-142">Requirement</span></span> | <span data-ttu-id="ef0dc-143">Valor</span><span class="sxs-lookup"><span data-stu-id="ef0dc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0dc-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef0dc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0dc-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ef0dc-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ef0dc-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef0dc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0dc-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef0dc-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ef0dc-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef0dc-148">Namespace</span></span><br/>                | <span data-ttu-id="ef0dc-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ef0dc-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef0dc-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ef0dc-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef0dc-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dc-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef0dc-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0dc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0dc-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dc-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef0dc-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef0dc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0dc-155">**\_BASEMETRICDEFINITION CIM**</span><span class="sxs-lookup"><span data-stu-id="ef0dc-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 

