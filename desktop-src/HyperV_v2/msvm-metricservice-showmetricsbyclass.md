---
description: Mostra as métricas por classe.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Método ShowMetricsByClass da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764685"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="37189-103">Método ShowMetricsByClass da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="37189-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="37189-104">Mostra as métricas por classe.</span><span class="sxs-lookup"><span data-stu-id="37189-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="37189-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37189-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="37189-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37189-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37189-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-108">Identifica uma classe CIM para a qual o método retorna referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem métricas que estão disponíveis para serem capturadas para todas as instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="37189-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="37189-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="37189-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-110">Identifica uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="37189-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="37189-111">O método retorna referências a instâncias de [**CIM \_ managedelement**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.</span><span class="sxs-lookup"><span data-stu-id="37189-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="37189-112">*Definitionlist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="37189-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-113">Após a conclusão bem-sucedida do método, o pode conter referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas disponíveis para coleta para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="37189-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37189-114">*Métricas* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="37189-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-115">Após a conclusão bem-sucedida do método, cada índice de matriz contém o valor da propriedade **Name** para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .</span><span class="sxs-lookup"><span data-stu-id="37189-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37189-116">*MetricCollectionEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="37189-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-117">Indica se uma métrica está sendo coletada para todas as instâncias de uma classe de elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="37189-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37189-118">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="37189-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37189-119">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="37189-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="37189-120">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="37189-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="37189-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="37189-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="37189-122">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="37189-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="37189-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="37189-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="37189-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37189-124">Return value</span></span>

<span data-ttu-id="37189-125">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="37189-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="37189-126">**Êxito** ()</span><span class="sxs-lookup"><span data-stu-id="37189-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="37189-127">**Sem suporte** ()</span><span class="sxs-lookup"><span data-stu-id="37189-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="37189-128">**Falha** ()</span><span class="sxs-lookup"><span data-stu-id="37189-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="37189-129">**Método reservado** ()</span><span class="sxs-lookup"><span data-stu-id="37189-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="37189-130">**Específico do fornecedor** ()</span><span class="sxs-lookup"><span data-stu-id="37189-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="37189-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37189-131">Requirements</span></span>



| <span data-ttu-id="37189-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="37189-132">Requirement</span></span> | <span data-ttu-id="37189-133">Valor</span><span class="sxs-lookup"><span data-stu-id="37189-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37189-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37189-134">Minimum supported client</span></span><br/> | <span data-ttu-id="37189-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="37189-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="37189-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37189-136">Minimum supported server</span></span><br/> | <span data-ttu-id="37189-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37189-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="37189-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="37189-138">Namespace</span></span><br/>                | <span data-ttu-id="37189-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="37189-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37189-140">MOF</span><span class="sxs-lookup"><span data-stu-id="37189-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37189-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37189-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37189-142">DLL</span><span class="sxs-lookup"><span data-stu-id="37189-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37189-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37189-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37189-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="37189-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37189-145">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="37189-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




