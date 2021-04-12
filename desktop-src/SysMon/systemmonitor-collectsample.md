---
title: Método SystemMonitor CollectSample
description: Obtém um valor para cada contador no objeto Counters.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Método CollectSample SysMon
- Método CollectSample SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, método CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455273"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="7a20c-106">Método SystemMonitor:: CollectSample</span><span class="sxs-lookup"><span data-stu-id="7a20c-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="7a20c-107">Obtém um valor para cada contador no objeto [**Counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="7a20c-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a20c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a20c-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="7a20c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a20c-109">Parameters</span></span>

<span data-ttu-id="7a20c-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7a20c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a20c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a20c-111">Return value</span></span>

<span data-ttu-id="7a20c-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7a20c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a20c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a20c-113">Remarks</span></span>

<span data-ttu-id="7a20c-114">Chame **CollectSample** somente se [**ManualUpdate**](systemmonitor-manualupdate.md) for true e você estiver obtendo valores de contador de amostragem da atividade atual do computador não use esse método durante a amostragem de um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7a20c-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="7a20c-115">O grafo ou relatório é atualizado com o novo valor.</span><span class="sxs-lookup"><span data-stu-id="7a20c-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="7a20c-116">Observe que alguns tipos de grafos precisam de dois exemplos para grafar os dados, por exemplo, o grafo de linha.</span><span class="sxs-lookup"><span data-stu-id="7a20c-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="7a20c-117">Para receber uma notificação quando o exemplo tiver sido coletado, implemente o evento [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .</span><span class="sxs-lookup"><span data-stu-id="7a20c-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a20c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a20c-118">Requirements</span></span>



| <span data-ttu-id="7a20c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a20c-119">Requirement</span></span> | <span data-ttu-id="7a20c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7a20c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a20c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a20c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a20c-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7a20c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7a20c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a20c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a20c-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7a20c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a20c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7a20c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a20c-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7a20c-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a20c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a20c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a20c-128">**Contadores**</span><span class="sxs-lookup"><span data-stu-id="7a20c-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="7a20c-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="7a20c-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





