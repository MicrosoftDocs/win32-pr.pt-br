---
description: Usado para controlar a coleção de métricas para um elemento ou elementos gerenciados.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Método ControlMetrics da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811876"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="42a36-103">Método ControlMetrics da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="42a36-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="42a36-104">Usado para controlar a coleção de métricas para um elemento ou elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="42a36-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a36-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42a36-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="42a36-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42a36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a36-107">*Assunto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42a36-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a36-108">Uma [**instância \_ gerenciada CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que identifica os elementos gerenciados para os quais as métricas serão coletadas.</span><span class="sxs-lookup"><span data-stu-id="42a36-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="42a36-109">Se esse parâmetro for **nulo**, as métricas para todos os elementos gerenciados associados ao parâmetro de *definição* serão coletadas.</span><span class="sxs-lookup"><span data-stu-id="42a36-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="42a36-110">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="42a36-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a36-111">Uma instância de [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que especifica quais métricas serão coletadas.</span><span class="sxs-lookup"><span data-stu-id="42a36-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="42a36-112">Se esse parâmetro for **nulo**, as métricas para todas as definições associadas ao elemento gerenciado identificado pelo parâmetro *Subject* serão coletadas</span><span class="sxs-lookup"><span data-stu-id="42a36-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="42a36-113">*MetricCollectionEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42a36-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a36-114">Especifica a operação a ser executada na coleção de métricas.</span><span class="sxs-lookup"><span data-stu-id="42a36-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="42a36-115">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="42a36-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="42a36-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="42a36-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="42a36-117">Habilitar a coleta de métricas.</span><span class="sxs-lookup"><span data-stu-id="42a36-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="42a36-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="42a36-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="42a36-119">Desabilitar a coleta de métricas.</span><span class="sxs-lookup"><span data-stu-id="42a36-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="42a36-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (4)</span><span class="sxs-lookup"><span data-stu-id="42a36-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="42a36-121">Redefinir valores de métricas.</span><span class="sxs-lookup"><span data-stu-id="42a36-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="42a36-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="42a36-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="42a36-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="42a36-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="42a36-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="42a36-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="42a36-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42a36-125">Return value</span></span>

<span data-ttu-id="42a36-126">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="42a36-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="42a36-127">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="42a36-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42a36-128">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="42a36-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42a36-129">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="42a36-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42a36-130">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="42a36-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="42a36-131">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="42a36-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="42a36-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="42a36-132">Remarks</span></span>

<span data-ttu-id="42a36-133">Esse método falhará nas seguintes instâncias:</span><span class="sxs-lookup"><span data-stu-id="42a36-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="42a36-134">Os parâmetros de *assunto* e *definição* são **nulos**.</span><span class="sxs-lookup"><span data-stu-id="42a36-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="42a36-135">Os parâmetros *Subject* e *Definition* não são **nulos** e não há uma instância de [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md) que associa as duas instâncias.</span><span class="sxs-lookup"><span data-stu-id="42a36-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="42a36-136">O parâmetro de *definição* é uma referência a uma instância de [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que não está associada com o [**Msvm \_ MetricService**](msvm-metricservice.md) por meio de [**Msvm \_ paraafetaelement**](msvm-serviceaffectselement.md).</span><span class="sxs-lookup"><span data-stu-id="42a36-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42a36-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a36-137">Requirements</span></span>



| <span data-ttu-id="42a36-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a36-138">Requirement</span></span> | <span data-ttu-id="42a36-139">Valor</span><span class="sxs-lookup"><span data-stu-id="42a36-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a36-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a36-140">Minimum supported client</span></span><br/> | <span data-ttu-id="42a36-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="42a36-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42a36-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a36-142">Minimum supported server</span></span><br/> | <span data-ttu-id="42a36-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="42a36-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42a36-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="42a36-144">Namespace</span></span><br/>                | <span data-ttu-id="42a36-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="42a36-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42a36-146">MOF</span><span class="sxs-lookup"><span data-stu-id="42a36-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42a36-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42a36-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42a36-148">DLL</span><span class="sxs-lookup"><span data-stu-id="42a36-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a36-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42a36-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42a36-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="42a36-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a36-151">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="42a36-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

