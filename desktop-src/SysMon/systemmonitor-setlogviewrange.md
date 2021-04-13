---
title: Método SystemMonitor. SetLogViewRange
description: Define a data de início usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Método SetLogViewRange SysMon
- Método SetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369407"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="8f14f-106">Método SystemMonitor. SetLogViewRange</span><span class="sxs-lookup"><span data-stu-id="8f14f-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="8f14f-107">Define a data de início usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8f14f-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f14f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f14f-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="8f14f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f14f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f14f-110">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f14f-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f14f-111">Data de início usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8f14f-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="8f14f-112">*StopTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f14f-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f14f-113">Data de término usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8f14f-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f14f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f14f-114">Return value</span></span>

<span data-ttu-id="8f14f-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f14f-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f14f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f14f-116">Remarks</span></span>

<span data-ttu-id="8f14f-117">O SYSMON recupera valores de contadores dos arquivos de log que se enquadram nas datas de início e parada, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8f14f-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="8f14f-118">Se você não especificar uma data de início ou se definir a data de início como um valor de data que está fora do intervalo de valores de data encontrado nos arquivos de log, o SYSMON alterará o valor para o valor de data mais antigo encontrado nos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8f14f-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="8f14f-119">Se o valor inicial for maior que o valor de parada, o SYSMON alterará o valor inicial para que seja o mesmo valor que o valor de parada.</span><span class="sxs-lookup"><span data-stu-id="8f14f-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="8f14f-120">Se você não especificar um valor de parada ou definir o valor de parada como um valor de data posterior à última data contida no arquivo de log, o SYSMON alterará o valor para o valor de data mais recente encontrado nos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8f14f-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="8f14f-121">Se o valor de parada for menor que o valor de parada, o SYSMON alterará o valor de parada para o mesmo valor que o valor inicial.</span><span class="sxs-lookup"><span data-stu-id="8f14f-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="8f14f-122">Se você especificar uma data de início e de parada, deverá especificar as datas antes de definir [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="8f14f-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="8f14f-123">Se você definir as datas após a definição de **SystemMonitor. DataSourceType**, somente o primeiro valor do contador será recuperado do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="8f14f-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f14f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f14f-124">Requirements</span></span>



| <span data-ttu-id="8f14f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f14f-125">Requirement</span></span> | <span data-ttu-id="8f14f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8f14f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f14f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f14f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8f14f-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f14f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f14f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f14f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8f14f-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8f14f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f14f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8f14f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f14f-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8f14f-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f14f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f14f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f14f-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="8f14f-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="8f14f-135">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="8f14f-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





