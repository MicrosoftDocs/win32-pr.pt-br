---
title: Propriedade SystemMonitor. UpdateInterval
description: Recupera ou define o período de tempo que o SYSMON espera antes da próxima vez que coleta dados do contador e atualiza o grafo ou relatório.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propriedade UpdateInterval SysMon
- Propriedade UpdateInterval SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918372"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="e4bca-106">Propriedade SystemMonitor. UpdateInterval</span><span class="sxs-lookup"><span data-stu-id="e4bca-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="e4bca-107">Recupera ou define o período de tempo que o SYSMON espera antes da próxima vez que coleta dados do contador e atualiza o grafo ou relatório.</span><span class="sxs-lookup"><span data-stu-id="e4bca-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="e4bca-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e4bca-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bca-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4bca-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="e4bca-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e4bca-110">Property value</span></span>

<span data-ttu-id="e4bca-111">Período de tempo, em segundos, que o SYSMON espera antes da próxima vez que coleta dados do contador e atualiza o grafo ou relatório.</span><span class="sxs-lookup"><span data-stu-id="e4bca-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="e4bca-112">O intervalo mínimo é de 1 segundo (esse também é o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="e4bca-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="e4bca-113">O valor máximo é 1 milhão.</span><span class="sxs-lookup"><span data-stu-id="e4bca-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4bca-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4bca-114">Remarks</span></span>

<span data-ttu-id="e4bca-115">Essa propriedade é relevante somente quando [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) é definido como false.</span><span class="sxs-lookup"><span data-stu-id="e4bca-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4bca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4bca-116">Requirements</span></span>



| <span data-ttu-id="e4bca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4bca-117">Requirement</span></span> | <span data-ttu-id="e4bca-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bca-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bca-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4bca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4bca-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4bca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e4bca-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4bca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4bca-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4bca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4bca-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e4bca-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4bca-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e4bca-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4bca-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e4bca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4bca-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e4bca-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





