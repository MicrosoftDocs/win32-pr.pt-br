---
description: Fornece a capacidade de retornar uma lista filtrada de \_ instâncias do CIM BaseMetricValue.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Método GetMetricValues da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758344"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a><span data-ttu-id="6a1fe-103">Método GetMetricValues da \_ classe METRICSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="6a1fe-103">GetMetricValues method of the CIM\_MetricService class</span></span>

<span data-ttu-id="6a1fe-104">Fornece a capacidade de retornar uma lista filtrada de instâncias do [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1fe-104">Provides the ability to return a filtered list of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a1fe-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="6a1fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a1fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a1fe-107">*Definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6a1fe-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a1fe-108">Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="6a1fe-109">*Intervalo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="6a1fe-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a1fe-110">Identifica como as instâncias são selecionadas.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="6a1fe-111">O algoritmo para instâncias de valor de ordenação é específico à definição de métrica.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-111">The algorithm for ordering value instances is metric-definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="6a1fe-112">**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="6a1fe-113">**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a1fe-114">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="6a1fe-115">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="6a1fe-116">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="6a1fe-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a1fe-117">Identifica o número máximo de instâncias a serem retornadas pelo método.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="6a1fe-118">*Valores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="6a1fe-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a1fe-119">Após a conclusão bem-sucedida do método, contém referências a instâncias do [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtradas de acordo com os valores dos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a1fe-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a1fe-120">Return value</span></span>

<span data-ttu-id="6a1fe-121">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6a1fe-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a1fe-122">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a1fe-123">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6a1fe-124">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6a1fe-125">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6a1fe-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6a1fe-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6a1fe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a1fe-127">Requirements</span></span>



| <span data-ttu-id="6a1fe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1fe-128">Requirement</span></span> | <span data-ttu-id="6a1fe-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6a1fe-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1fe-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a1fe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6a1fe-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6a1fe-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6a1fe-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a1fe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6a1fe-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a1fe-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6a1fe-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a1fe-134">Namespace</span></span><br/>                | <span data-ttu-id="6a1fe-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6a1fe-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a1fe-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6a1fe-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a1fe-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a1fe-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a1fe-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6a1fe-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a1fe-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a1fe-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a1fe-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a1fe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1fe-141">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6a1fe-141">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




