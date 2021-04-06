---
description: 'Relata o seguinte: as métricas disponíveis para serem coletadas para todas as instâncias de uma classe CIM, as classes CIM para as quais uma métrica definida por uma instância do CIM \_ BaseMetricDefinition está disponível para ser coletada e se uma métrica específica está sendo coletada ou não para um elemento gerenciado.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Método ShowMetricsByClass da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828600"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="ed8fa-103">Método ShowMetricsByClass da \_ classe METRICSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="ed8fa-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="ed8fa-104">Relata o seguinte: as métricas disponíveis para serem coletadas para todas as instâncias de uma classe CIM, as classes CIM para as quais uma métrica definida por uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) está disponível para ser coletada e se uma métrica específica está sendo coletada ou não para um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ed8fa-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed8fa-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="ed8fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed8fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8fa-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed8fa-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8fa-108">Identifica uma classe CIM para a qual o método retorna referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem métricas que estão disponíveis para serem capturadas para todas as instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="ed8fa-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="ed8fa-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ed8fa-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8fa-110">Identifica uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ed8fa-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="ed8fa-111">O método retorna referências a instâncias de [**CIM \_ managedelement**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.</span><span class="sxs-lookup"><span data-stu-id="ed8fa-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="ed8fa-112">*Definitionlist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed8fa-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8fa-113">Em caso de sucesso, pode conter referências a instâncias de objetos [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) que definem métricas disponíveis para coleta para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="ed8fa-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ed8fa-114">*Métricas* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed8fa-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8fa-115">Em caso de sucesso, cada índice de matriz deve conter o valor da propriedade **Name** para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .</span><span class="sxs-lookup"><span data-stu-id="ed8fa-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ed8fa-116">*MetricCollectionEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed8fa-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8fa-117">Indica se uma métrica está sendo coletada para todas as instâncias de uma classe de elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="ed8fa-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ed8fa-118">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ed8fa-119">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="ed8fa-120">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ed8fa-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ed8fa-122">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="ed8fa-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ed8fa-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ed8fa-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed8fa-124">Return value</span></span>

<span data-ttu-id="ed8fa-125">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ed8fa-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ed8fa-126">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed8fa-127">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ed8fa-128">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ed8fa-129">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ed8fa-130">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ed8fa-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ed8fa-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed8fa-131">Requirements</span></span>



| <span data-ttu-id="ed8fa-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8fa-132">Requirement</span></span> | <span data-ttu-id="ed8fa-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ed8fa-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8fa-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed8fa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8fa-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ed8fa-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ed8fa-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed8fa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8fa-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ed8fa-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ed8fa-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed8fa-138">Namespace</span></span><br/>                | <span data-ttu-id="ed8fa-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ed8fa-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ed8fa-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ed8fa-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed8fa-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed8fa-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed8fa-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ed8fa-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed8fa-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed8fa-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed8fa-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed8fa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8fa-145">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ed8fa-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




