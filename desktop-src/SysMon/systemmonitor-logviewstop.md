---
title: Propriedade SystemMonitor. LogViewStop
description: Recupera ou define a data de término usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propriedade LogViewStop SysMon
- Propriedade LogViewStop SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918409"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="83973-106">Propriedade SystemMonitor. LogViewStop</span><span class="sxs-lookup"><span data-stu-id="83973-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="83973-107">Recupera ou define a data de término usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="83973-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="83973-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="83973-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83973-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83973-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="83973-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="83973-110">Property value</span></span>

<span data-ttu-id="83973-111">Data de término usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="83973-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="83973-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="83973-112">Remarks</span></span>

<span data-ttu-id="83973-113">O SYSMON recupera valores de contadores dos arquivos de log que se enquadram dentro de [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e de datas de parada, inclusive.</span><span class="sxs-lookup"><span data-stu-id="83973-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="83973-114">Se você não especificar um valor de parada ou definir essa propriedade como um valor de data posterior à última data contida no arquivo de log, o SYSMON alterará o valor para o valor de data mais recente encontrado nos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="83973-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="83973-115">Se essa propriedade for definida como um valor de data menor que [**LogViewStart**](systemmonitor-logviewstart.md), o SYSMON alterará o valor para o valor de **LogViewStart**.</span><span class="sxs-lookup"><span data-stu-id="83973-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="83973-116">Você deve definir a data de início antes de definir a data de parada; caso contrário, ambos os valores são definidos como Date. MinValue e, se você definir as datas após a definição de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md), somente o primeiro valor do contador será recuperado do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="83973-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="83973-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83973-117">Requirements</span></span>



| <span data-ttu-id="83973-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83973-118">Requirement</span></span> | <span data-ttu-id="83973-119">Valor</span><span class="sxs-lookup"><span data-stu-id="83973-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83973-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83973-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83973-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83973-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="83973-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83973-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83973-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83973-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83973-124">DLL</span><span class="sxs-lookup"><span data-stu-id="83973-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83973-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="83973-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83973-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="83973-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83973-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="83973-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="83973-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="83973-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="83973-129">**SystemMonitor.LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="83973-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="83973-130">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="83973-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="83973-131">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="83973-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





