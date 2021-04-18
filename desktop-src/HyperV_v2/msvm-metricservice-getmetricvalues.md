---
description: Obtém valores de métrica.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Método GetMetricValues da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787520"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="d2751-103">Método GetMetricValues da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="d2751-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="d2751-104">Obtém valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="d2751-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2751-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2751-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="d2751-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2751-107">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d2751-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2751-108">Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="d2751-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="d2751-109">*Intervalo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="d2751-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2751-110">Identifica como as instâncias são selecionadas.</span><span class="sxs-lookup"><span data-stu-id="d2751-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="d2751-111">O algoritmo para instâncias de valor de ordenação é específico à definição de métrica.</span><span class="sxs-lookup"><span data-stu-id="d2751-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="d2751-112">**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="d2751-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="d2751-113">**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="d2751-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d2751-114">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d2751-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="d2751-115">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d2751-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d2751-116">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="d2751-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2751-117">Identifica o número máximo de instâncias a serem retornadas pelo método.</span><span class="sxs-lookup"><span data-stu-id="d2751-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="d2751-118">*Valores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="d2751-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2751-119">Após a conclusão bem-sucedida do método, contém referências a instâncias do [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtradas de acordo com os valores dos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="d2751-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2751-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2751-120">Return value</span></span>

<span data-ttu-id="d2751-121">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d2751-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d2751-122">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="d2751-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2751-123">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="d2751-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2751-124">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="d2751-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2751-125">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d2751-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2751-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d2751-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d2751-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2751-127">Requirements</span></span>



| <span data-ttu-id="d2751-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2751-128">Requirement</span></span> | <span data-ttu-id="d2751-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d2751-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2751-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2751-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d2751-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d2751-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d2751-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2751-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d2751-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d2751-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d2751-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2751-134">Namespace</span></span><br/>                | <span data-ttu-id="d2751-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d2751-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d2751-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d2751-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2751-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2751-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2751-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d2751-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2751-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2751-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2751-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2751-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2751-141">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="d2751-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




