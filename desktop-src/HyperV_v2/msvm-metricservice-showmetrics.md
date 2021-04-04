---
description: Mostra as métricas especificadas.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Método de permétricas da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837133"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="dec32-103">Método de permétricas da \_ classe Msvm MetricService</span><span class="sxs-lookup"><span data-stu-id="dec32-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="dec32-104">Mostra as métricas especificadas.</span><span class="sxs-lookup"><span data-stu-id="dec32-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dec32-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="dec32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dec32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec32-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dec32-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec32-108">O parâmetro Subject identifica uma instância de [**CIM \_ managedelement**](cim-managedelement.md) para a qual o método retorna referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas que estão sendo capturadas para o **CIM \_ managedelement**.</span><span class="sxs-lookup"><span data-stu-id="dec32-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="dec32-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="dec32-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec32-110">O parâmetro de definição identifica uma instância [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="dec32-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="dec32-111">O método retorna referências a instâncias de [**CIM \_ managedelement**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.</span><span class="sxs-lookup"><span data-stu-id="dec32-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="dec32-112">*ManagedElements* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dec32-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec32-113">Após a conclusão bem-sucedida do método, o  \[ \] parâmetro ManagedElements pode conter referências ao [**CIM \_ managedelement**](cim-managedelement.md) para o qual a métrica identificada pelo parâmetro de *definição* está disponível para coleta.</span><span class="sxs-lookup"><span data-stu-id="dec32-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="dec32-114">*Definitionlist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dec32-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec32-115">Após a conclusão bem-sucedida do método, o parâmetro *definitionlist* pode conter referências a instâncias de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas disponíveis para a coleção para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="dec32-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dec32-116">*Métricas* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dec32-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec32-117">Após a conclusão bem-sucedida do método, cada índice de matriz do parâmetro *metricnames* deverá conter o valor da propriedade Name para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .</span><span class="sxs-lookup"><span data-stu-id="dec32-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dec32-118">*MetricCollectionEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dec32-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec32-119">O parâmetro *MetricCollectionEnabled* indica se uma métrica está sendo coletada para um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dec32-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="dec32-120">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="dec32-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="dec32-121">**Desabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="dec32-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="dec32-122">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="dec32-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dec32-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dec32-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="dec32-124">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dec32-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="dec32-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dec32-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="dec32-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dec32-126">Return value</span></span>

<span data-ttu-id="dec32-127">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dec32-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dec32-128">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="dec32-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dec32-129">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="dec32-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dec32-130">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="dec32-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dec32-131">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dec32-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dec32-132">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dec32-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dec32-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec32-133">Requirements</span></span>



| <span data-ttu-id="dec32-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec32-134">Requirement</span></span> | <span data-ttu-id="dec32-135">Valor</span><span class="sxs-lookup"><span data-stu-id="dec32-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec32-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec32-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dec32-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dec32-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dec32-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec32-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dec32-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dec32-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dec32-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="dec32-140">Namespace</span></span><br/>                | <span data-ttu-id="dec32-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dec32-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dec32-142">MOF</span><span class="sxs-lookup"><span data-stu-id="dec32-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dec32-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dec32-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dec32-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dec32-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec32-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dec32-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dec32-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec32-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec32-147">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="dec32-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




