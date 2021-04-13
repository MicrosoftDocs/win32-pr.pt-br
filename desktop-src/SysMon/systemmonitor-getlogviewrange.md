---
title: Método SystemMonitor. GetLogViewRange
description: Recupera a data de início usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Método GetLogViewRange SysMon
- Método GetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499381"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="9b6a0-106">Método SystemMonitor. GetLogViewRange</span><span class="sxs-lookup"><span data-stu-id="9b6a0-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="9b6a0-107">Recupera a data de início usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6a0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b6a0-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="9b6a0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b6a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6a0-110">*StartTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b6a0-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6a0-111">Data de início usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="9b6a0-112">*StopTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b6a0-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6a0-113">Data de término usada para recuperar valores de contadores dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6a0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b6a0-114">Return value</span></span>

<span data-ttu-id="9b6a0-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b6a0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b6a0-116">Remarks</span></span>

<span data-ttu-id="9b6a0-117">O SYSMON recupera valores de contadores dos arquivos de log que se enquadram nas datas de início e parada, inclusive.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="9b6a0-118">Usar esse método é o mesmo que acessar as propriedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) .</span><span class="sxs-lookup"><span data-stu-id="9b6a0-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6a0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b6a0-119">Requirements</span></span>



| <span data-ttu-id="9b6a0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b6a0-120">Requirement</span></span> | <span data-ttu-id="9b6a0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9b6a0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6a0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b6a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6a0-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b6a0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b6a0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b6a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6a0-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b6a0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b6a0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9b6a0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b6a0-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9b6a0-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b6a0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b6a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6a0-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="9b6a0-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="9b6a0-130">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="9b6a0-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





