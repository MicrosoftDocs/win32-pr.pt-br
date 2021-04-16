---
description: Controla as métricas por classe.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Método ControlMetricsByClass da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759238"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="9d763-103">Método ControlMetricsByClass da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="9d763-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="9d763-104">Controla as métricas por classe.</span><span class="sxs-lookup"><span data-stu-id="9d763-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d763-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d763-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="9d763-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d763-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d763-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d763-108">Identifica a classe CIM para a qual as métricas serão controladas.</span><span class="sxs-lookup"><span data-stu-id="9d763-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="9d763-109">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9d763-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d763-110">Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão controladas.</span><span class="sxs-lookup"><span data-stu-id="9d763-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="9d763-111">*MetricCollectionEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d763-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d763-112">Indica a operação desejada a ser executada nas métricas.</span><span class="sxs-lookup"><span data-stu-id="9d763-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="9d763-113">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="9d763-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="9d763-114">**Desabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="9d763-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="9d763-115">**Redefinir** (4)</span><span class="sxs-lookup"><span data-stu-id="9d763-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9d763-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9d763-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9d763-117">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9d763-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="9d763-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9d763-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9d763-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d763-119">Return value</span></span>

<span data-ttu-id="9d763-120">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9d763-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9d763-121">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="9d763-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d763-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="9d763-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d763-123">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="9d763-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d763-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9d763-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9d763-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9d763-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9d763-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d763-126">Requirements</span></span>



| <span data-ttu-id="9d763-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d763-127">Requirement</span></span> | <span data-ttu-id="9d763-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9d763-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d763-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d763-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9d763-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9d763-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9d763-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d763-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9d763-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9d763-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9d763-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d763-133">Namespace</span></span><br/>                | <span data-ttu-id="9d763-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9d763-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9d763-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9d763-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d763-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d763-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d763-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9d763-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d763-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d763-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d763-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d763-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d763-140">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="9d763-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




