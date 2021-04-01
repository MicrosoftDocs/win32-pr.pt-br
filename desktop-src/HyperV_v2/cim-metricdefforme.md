---
description: Representa uma associação na qual um \_ objeto CIM BaseMetricDefinition define métricas para um elemento gerenciado.
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: Classe CIM_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829039"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="46a6b-103">\_Classe CIM MetricDefForME</span><span class="sxs-lookup"><span data-stu-id="46a6b-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="46a6b-104">Representa uma associação na qual um objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) define métricas para um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46a6b-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46a6b-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="46a6b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="46a6b-106">Members</span></span>

<span data-ttu-id="46a6b-107">A classe **CIM \_ MetricDefForME** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="46a6b-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="46a6b-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46a6b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46a6b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46a6b-109">Properties</span></span>

<span data-ttu-id="46a6b-110">A classe **CIM \_ MetricDefForME** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="46a6b-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46a6b-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="46a6b-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6b-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="46a6b-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="46a6b-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46a6b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6b-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="46a6b-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="46a6b-115">O elemento gerenciado que está associado à definição de métrica.</span><span class="sxs-lookup"><span data-stu-id="46a6b-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="46a6b-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="46a6b-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6b-117">Tipo de dados: **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="46a6b-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="46a6b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46a6b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6b-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="46a6b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="46a6b-120">A definição de métrica que está associada ao elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46a6b-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="46a6b-121">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="46a6b-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6b-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6b-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46a6b-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46a6b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6b-124">Indica se a métrica está sendo coletada para o elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="46a6b-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46a6b-125">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="46a6b-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46a6b-126">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="46a6b-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="46a6b-127">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="46a6b-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="46a6b-128">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="46a6b-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="46a6b-129">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="46a6b-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="46a6b-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46a6b-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="46a6b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46a6b-131">Requirements</span></span>



| <span data-ttu-id="46a6b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a6b-132">Requirement</span></span> | <span data-ttu-id="46a6b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="46a6b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a6b-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46a6b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="46a6b-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="46a6b-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="46a6b-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46a6b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="46a6b-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46a6b-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="46a6b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="46a6b-138">Namespace</span></span><br/>                | <span data-ttu-id="46a6b-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="46a6b-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46a6b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="46a6b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46a6b-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46a6b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46a6b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="46a6b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46a6b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46a6b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46a6b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="46a6b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a6b-145">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="46a6b-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

