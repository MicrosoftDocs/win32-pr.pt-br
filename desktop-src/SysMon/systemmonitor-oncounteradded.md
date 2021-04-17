---
title: Evento SystemMonitor. OnCounterAdded
description: Notifica quando um contador é adicionado à coleção de contadores.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Evento OnCounterAdded do SysMon
- Evento OnCounterAdded SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterAdded
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753904"
---
# <a name="systemmonitoroncounteradded-event"></a><span data-ttu-id="7df23-106">Evento SystemMonitor. OnCounterAdded</span><span class="sxs-lookup"><span data-stu-id="7df23-106">SystemMonitor.OnCounterAdded event</span></span>

<span data-ttu-id="7df23-107">Notifica quando um contador é adicionado à coleção de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="7df23-107">Notifies you when a counter is added to the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df23-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7df23-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="7df23-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7df23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df23-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7df23-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df23-111">Índice do contador adicionado ao objeto da coleção de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="7df23-111">Index of the counter added to the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df23-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7df23-112">Return value</span></span>

<span data-ttu-id="7df23-113">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7df23-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df23-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df23-114">Requirements</span></span>



| <span data-ttu-id="7df23-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df23-115">Requirement</span></span> | <span data-ttu-id="7df23-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7df23-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7df23-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7df23-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7df23-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7df23-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7df23-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7df23-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7df23-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7df23-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df23-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7df23-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df23-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df23-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df23-124">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="7df23-124">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[<span data-ttu-id="7df23-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="7df23-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





