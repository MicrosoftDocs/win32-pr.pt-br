---
title: Método SystemMonitor. ScaleToFit
description: Dimensionar valores do contador para caber no grafo.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Método ScaleToFit SysMon
- Método ScaleToFit SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644552"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="cf638-106">Método SystemMonitor. ScaleToFit</span><span class="sxs-lookup"><span data-stu-id="cf638-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="cf638-107">Dimensionar valores do contador para caber no grafo.</span><span class="sxs-lookup"><span data-stu-id="cf638-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf638-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf638-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="cf638-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf638-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf638-110">*selectedCountersOnly* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cf638-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf638-111">True para dimensionar apenas os contadores selecionados; caso contrário, false para dimensionar todos os contadores.</span><span class="sxs-lookup"><span data-stu-id="cf638-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf638-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf638-112">Return value</span></span>

<span data-ttu-id="cf638-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cf638-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf638-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf638-114">Remarks</span></span>

<span data-ttu-id="cf638-115">Esse método limpará o modo de exibição de gráfico.</span><span class="sxs-lookup"><span data-stu-id="cf638-115">This method will clear the graph view.</span></span> <span data-ttu-id="cf638-116">O SYSMON usa o fator de escala especificado para cada contador para redesenhar o grafo se a fonte de dados for um arquivo de log ou começar a grafar novos valores de contador se a fonte de dados for uma atividade em tempo real.</span><span class="sxs-lookup"><span data-stu-id="cf638-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf638-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf638-117">Requirements</span></span>



| <span data-ttu-id="cf638-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf638-118">Requirement</span></span> | <span data-ttu-id="cf638-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cf638-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf638-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf638-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cf638-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf638-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf638-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf638-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cf638-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf638-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf638-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cf638-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf638-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cf638-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf638-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cf638-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf638-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="cf638-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="cf638-128">**MYITEM. ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="cf638-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="cf638-129">**Coitem. selecionado**</span><span class="sxs-lookup"><span data-stu-id="cf638-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





