---
description: Habilita e desabilita a coleção de métricas.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Método ControlMetrics da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169737"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="e2651-103">Método ControlMetrics da \_ classe METRICSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="e2651-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="e2651-104">Habilita e desabilita a coleção de métricas. **ControlMetrics** é usado para controlar a coleção de cada tipo de métrica para um [**CIM \_ managedelement**](cim-managedelement.md), a coleção de um determinado tipo de métrica para todos os elementos gerenciados ou a coleção de uma métrica específica para um elemento gerenciado específico.</span><span class="sxs-lookup"><span data-stu-id="e2651-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2651-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2651-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="e2651-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2651-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2651-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2651-108">Um [**\_ managedelement do CIM**](cim-managedelement.md) que identifica os elementos gerenciados para os quais as métricas serão controladas.</span><span class="sxs-lookup"><span data-stu-id="e2651-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="e2651-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e2651-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2651-110">Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão controladas.</span><span class="sxs-lookup"><span data-stu-id="e2651-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="e2651-111">*MetricCollectionEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2651-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2651-112">Indica a operação desejada a ser executada nas métricas.</span><span class="sxs-lookup"><span data-stu-id="e2651-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="e2651-113">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="e2651-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="e2651-114">**Desabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="e2651-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e2651-115">**Redefinir** (4)</span><span class="sxs-lookup"><span data-stu-id="e2651-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e2651-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e2651-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e2651-117">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e2651-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="e2651-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2651-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="e2651-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2651-119">Return value</span></span>

<span data-ttu-id="e2651-120">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e2651-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e2651-121">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="e2651-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2651-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="e2651-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2651-123">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="e2651-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2651-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e2651-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e2651-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e2651-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2651-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2651-126">Requirements</span></span>



| <span data-ttu-id="e2651-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2651-127">Requirement</span></span> | <span data-ttu-id="e2651-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e2651-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2651-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2651-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2651-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e2651-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e2651-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2651-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2651-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e2651-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e2651-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2651-133">Namespace</span></span><br/>                | <span data-ttu-id="e2651-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e2651-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e2651-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e2651-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2651-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2651-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2651-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e2651-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2651-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2651-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2651-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2651-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2651-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e2651-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




