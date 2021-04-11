---
description: Define os tempos de exemplo de controle.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Método ControlSampleTimes da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169414"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="5c002-103">Método ControlSampleTimes da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="5c002-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="5c002-104">Define os tempos de exemplo de controle.</span><span class="sxs-lookup"><span data-stu-id="5c002-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c002-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c002-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="5c002-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c002-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c002-107">*StartSampleTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c002-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-108">Ponto no tempo em que a amostragem para as métricas deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="5c002-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="5c002-109">Um valor de 99990101000000.000000 + 000 deverá indicar que a amostragem deve ser iniciada na próxima vez que for sincronizada com a hora completa.</span><span class="sxs-lookup"><span data-stu-id="5c002-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="5c002-110">A amostragem será sincronizada com a hora completa se segundos desde o intervalo de amostragem de módulo de meia-noite em segundos for igual a 0.</span><span class="sxs-lookup"><span data-stu-id="5c002-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-111">*PreferredSampleInterval* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c002-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-112">Tempo de intervalo de amostragem preferencial.</span><span class="sxs-lookup"><span data-stu-id="5c002-112">Preferred sample interval time.</span></span> <span data-ttu-id="5c002-113">Para obter métricas correlacionadas, é recomendável que o intervalo de exemplo seja escolhido de forma que o tempo de intervalo de amostragem de 3600 de módulo em segundos seja igual a 0.</span><span class="sxs-lookup"><span data-stu-id="5c002-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="5c002-114">É responsabilidade da implementação do serviço de métrica CIM decidir se o tempo de intervalo de amostragem solicitado é respeitado.</span><span class="sxs-lookup"><span data-stu-id="5c002-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="5c002-115">O cliente CIM pode verificar se os provedores de métrica estão respeitando o tempo de intervalo de amostragem solicitado, recuperando instâncias BaseMetricDefinition relacionadas e verificando o conteúdo da propriedade "CIM \_ BaseMetricDefinition. SampleInterval".</span><span class="sxs-lookup"><span data-stu-id="5c002-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-116">*RestartGathering* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c002-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-117">Booliano que quando definido como verdadeiro solicita que a coleta de todas as métricas associadas ao serviço de métrica seja reiniciada com essa chamada de método.</span><span class="sxs-lookup"><span data-stu-id="5c002-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c002-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c002-118">Return value</span></span>

<span data-ttu-id="5c002-119">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5c002-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5c002-120">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="5c002-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c002-121">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5c002-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c002-122">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="5c002-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c002-123">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c002-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c002-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5c002-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5c002-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c002-125">Requirements</span></span>



| <span data-ttu-id="5c002-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c002-126">Requirement</span></span> | <span data-ttu-id="5c002-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5c002-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c002-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c002-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c002-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5c002-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5c002-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c002-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c002-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5c002-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5c002-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c002-132">Namespace</span></span><br/>                | <span data-ttu-id="5c002-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5c002-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5c002-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5c002-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c002-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c002-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5c002-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c002-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c002-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c002-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c002-139">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="5c002-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




