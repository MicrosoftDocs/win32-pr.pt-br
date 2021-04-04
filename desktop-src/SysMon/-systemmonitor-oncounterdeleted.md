---
title: Evento SystemMonitor. OnCounterDeleted
description: Notifica você antes de um contador ser excluído da coleção de contadores.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Evento OnCounterDeleted do SysMon
- Evento OnCounterDeleted SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918502"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="cbaae-106">Evento SystemMonitor. OnCounterDeleted</span><span class="sxs-lookup"><span data-stu-id="cbaae-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="cbaae-107">Notifica você antes de um contador ser excluído da coleção de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="cbaae-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbaae-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbaae-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="cbaae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbaae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbaae-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cbaae-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbaae-111">Índice do contador a ser excluído do objeto da coleção de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="cbaae-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbaae-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbaae-112">Return value</span></span>

<span data-ttu-id="cbaae-113">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cbaae-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbaae-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbaae-114">Requirements</span></span>



| <span data-ttu-id="cbaae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbaae-115">Requirement</span></span> | <span data-ttu-id="cbaae-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cbaae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbaae-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbaae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cbaae-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cbaae-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cbaae-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbaae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cbaae-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cbaae-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cbaae-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cbaae-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbaae-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cbaae-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbaae-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbaae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbaae-124">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="cbaae-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="cbaae-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="cbaae-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





