---
title: Propriedade SystemMonitor. LogViewStart
description: Recupera ou define a data de início usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Propriedade LogViewStart SysMon
- Propriedade LogViewStart SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918317"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="bcb78-106">Propriedade SystemMonitor. LogViewStart</span><span class="sxs-lookup"><span data-stu-id="bcb78-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="bcb78-107">Recupera ou define a data de início usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="bcb78-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="bcb78-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bcb78-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb78-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcb78-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="bcb78-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bcb78-110">Property value</span></span>

<span data-ttu-id="bcb78-111">Data de início usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="bcb78-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb78-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcb78-112">Remarks</span></span>

<span data-ttu-id="bcb78-113">O SYSMON recupera valores de contadores dos arquivos de log que se enquadram nas datas inicial e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) , inclusive.</span><span class="sxs-lookup"><span data-stu-id="bcb78-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="bcb78-114">Se você não especificar uma data de início ou se definir essa propriedade como um valor de data que está fora do intervalo de valores de data encontrado nos arquivos de log, o SYSMON alterará o valor para o valor de data mais anterior encontrado nos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="bcb78-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="bcb78-115">Se essa propriedade for definida como um valor de data maior que [**LogViewStop**](systemmonitor-logviewstop.md), o SYSMON alterará o valor para o valor de **LogViewStop**.</span><span class="sxs-lookup"><span data-stu-id="bcb78-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="bcb78-116">Se você especificar uma data de início e de parada, deverá especificar as datas antes de definir [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="bcb78-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb78-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb78-117">Requirements</span></span>



| <span data-ttu-id="bcb78-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb78-118">Requirement</span></span> | <span data-ttu-id="bcb78-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb78-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb78-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcb78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb78-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bcb78-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bcb78-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcb78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb78-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bcb78-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcb78-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb78-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcb78-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bcb78-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb78-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcb78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb78-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="bcb78-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="bcb78-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="bcb78-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="bcb78-129">**SystemMonitor. LogFiles**</span><span class="sxs-lookup"><span data-stu-id="bcb78-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="bcb78-130">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="bcb78-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="bcb78-131">**SystemMonitor.LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="bcb78-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="bcb78-132">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="bcb78-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





