---
description: Permite que a especificação do ponto no tempo coleta de métricas seja iniciada e especifique o tempo de intervalo de exemplo preferencial para a coleta de dados periódicas.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Método ControlSampleTimes da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758806"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="89c21-103">Método ControlSampleTimes da \_ classe METRICSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="89c21-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="89c21-104">Permite que a especificação do ponto no tempo coleta de métricas seja iniciada e especifique o tempo de intervalo de exemplo preferencial para a coleta de dados periódicas.</span><span class="sxs-lookup"><span data-stu-id="89c21-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="89c21-105">Sempre que a amostragem de métricas adicionais é iniciada, as configurações especificadas por esse método podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="89c21-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c21-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89c21-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="89c21-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89c21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c21-108">*StartSampleTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89c21-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c21-109">Ponto no tempo em que a amostragem para as métricas deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="89c21-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="89c21-110">Um valor de 99990101000000.000000 + 000 deverá indicar que a amostragem deve ser iniciada na próxima vez que for sincronizada com a hora completa.</span><span class="sxs-lookup"><span data-stu-id="89c21-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="89c21-111">A amostragem será sincronizada com a hora completa se segundos desde o intervalo de amostragem de módulo de meia-noite em segundos for igual a 0.</span><span class="sxs-lookup"><span data-stu-id="89c21-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="89c21-112">*PreferredSampleInterval* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89c21-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c21-113">Tempo de intervalo de amostragem preferencial.</span><span class="sxs-lookup"><span data-stu-id="89c21-113">Preferred sample interval time.</span></span> <span data-ttu-id="89c21-114">Para obter métricas correlacionadas, é recomendável que o intervalo de exemplo seja escolhido de forma que o tempo de intervalo de amostragem de 3600 de módulo em segundos seja igual a 0.</span><span class="sxs-lookup"><span data-stu-id="89c21-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="89c21-115">É responsabilidade da implementação do serviço de métrica CIM decidir se o tempo de intervalo de amostragem solicitado é respeitado.</span><span class="sxs-lookup"><span data-stu-id="89c21-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="89c21-116">O cliente CIM pode verificar se os provedores de métrica estão respeitando o tempo de intervalo de amostragem solicitado, recuperando instâncias BaseMetricDefinition relacionadas e verificando o conteúdo [**do \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).**Propriedade SampleInterval** .</span><span class="sxs-lookup"><span data-stu-id="89c21-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="89c21-117">*RestartGathering* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89c21-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c21-118">**True** para solicitar que a coleta de todas as métricas associadas ao serviço de métrica seja reiniciada com essa chamada de método.</span><span class="sxs-lookup"><span data-stu-id="89c21-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c21-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89c21-119">Return value</span></span>

<span data-ttu-id="89c21-120">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="89c21-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="89c21-121">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="89c21-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="89c21-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="89c21-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="89c21-123">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="89c21-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c21-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="89c21-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="89c21-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="89c21-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="89c21-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89c21-126">Requirements</span></span>



| <span data-ttu-id="89c21-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c21-127">Requirement</span></span> | <span data-ttu-id="89c21-128">Valor</span><span class="sxs-lookup"><span data-stu-id="89c21-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c21-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89c21-129">Minimum supported client</span></span><br/> | <span data-ttu-id="89c21-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="89c21-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="89c21-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89c21-131">Minimum supported server</span></span><br/> | <span data-ttu-id="89c21-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="89c21-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="89c21-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="89c21-133">Namespace</span></span><br/>                | <span data-ttu-id="89c21-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="89c21-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="89c21-135">MOF</span><span class="sxs-lookup"><span data-stu-id="89c21-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89c21-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89c21-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89c21-137">DLL</span><span class="sxs-lookup"><span data-stu-id="89c21-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c21-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89c21-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89c21-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="89c21-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c21-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="89c21-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




