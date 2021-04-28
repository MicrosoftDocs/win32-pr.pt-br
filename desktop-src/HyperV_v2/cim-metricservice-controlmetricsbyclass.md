---
description: Método ControlMetricsByClass da classe CIM_MetricService – habilita e desabilita a coleção de métricas.
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Método ControlMetricsByClass da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109704"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="49bc9-103">Método ControlMetricsByClass da \_ classe METRICSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="49bc9-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="49bc9-104">Habilita e desabilita a coleção de métricas. **ControlMetricsByClass** é usado para controlar a coleção de cada tipo de métrica para todas as instâncias de uma classe ou a coleção de uma métrica específica para todas as instâncias de uma classe.</span><span class="sxs-lookup"><span data-stu-id="49bc9-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="49bc9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49bc9-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="49bc9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49bc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49bc9-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49bc9-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49bc9-108">Identifica a classe [**CIM \_ managedelement**](cim-managedelement.md) para a qual as métricas serão controladas.</span><span class="sxs-lookup"><span data-stu-id="49bc9-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="49bc9-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="49bc9-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49bc9-110">Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão controladas.</span><span class="sxs-lookup"><span data-stu-id="49bc9-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="49bc9-111">*MetricCollectionEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49bc9-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49bc9-112">Indica a operação desejada a ser executada nas métricas.</span><span class="sxs-lookup"><span data-stu-id="49bc9-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="49bc9-113">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="49bc9-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="49bc9-114">**Desabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="49bc9-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="49bc9-115">**Redefinir** (4)</span><span class="sxs-lookup"><span data-stu-id="49bc9-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="49bc9-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="49bc9-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="49bc9-117">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="49bc9-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="49bc9-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="49bc9-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="49bc9-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="49bc9-119">Return value</span></span>

<span data-ttu-id="49bc9-120">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="49bc9-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="49bc9-121">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="49bc9-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="49bc9-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="49bc9-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="49bc9-123">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="49bc9-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="49bc9-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="49bc9-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="49bc9-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="49bc9-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="49bc9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49bc9-126">Requirements</span></span>



| <span data-ttu-id="49bc9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="49bc9-127">Requirement</span></span> | <span data-ttu-id="49bc9-128">Valor</span><span class="sxs-lookup"><span data-stu-id="49bc9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49bc9-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49bc9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="49bc9-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="49bc9-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="49bc9-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49bc9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="49bc9-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="49bc9-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="49bc9-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="49bc9-133">Namespace</span></span><br/>                | <span data-ttu-id="49bc9-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="49bc9-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="49bc9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="49bc9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49bc9-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49bc9-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="49bc9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="49bc9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49bc9-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="49bc9-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="49bc9-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="49bc9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49bc9-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="49bc9-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




