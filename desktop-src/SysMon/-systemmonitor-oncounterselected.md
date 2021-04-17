---
title: Evento SystemMonitor. OnCounterSelected
description: Notifica quando um contador é selecionado.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Evento OnCounterSelected do SysMon
- Evento OnCounterSelected SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754923"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="90196-106">Evento SystemMonitor. OnCounterSelected</span><span class="sxs-lookup"><span data-stu-id="90196-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="90196-107">Notifica quando um contador é selecionado.</span><span class="sxs-lookup"><span data-stu-id="90196-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="90196-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90196-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="90196-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90196-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90196-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="90196-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90196-111">Índice do contador selecionado no objeto da coleção de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="90196-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90196-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90196-112">Return value</span></span>

<span data-ttu-id="90196-113">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="90196-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90196-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="90196-114">Remarks</span></span>

<span data-ttu-id="90196-115">Você pode receber esse evento quando</span><span class="sxs-lookup"><span data-stu-id="90196-115">You can receive this event when</span></span>

-   <span data-ttu-id="90196-116">Você define o [**MyItem. Selected**](counteritem-selected.md) como true</span><span class="sxs-lookup"><span data-stu-id="90196-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="90196-117">O usuário seleciona um contador na legenda</span><span class="sxs-lookup"><span data-stu-id="90196-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="90196-118">O usuário clica duas vezes em um contador na legenda</span><span class="sxs-lookup"><span data-stu-id="90196-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="90196-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90196-119">Requirements</span></span>



| <span data-ttu-id="90196-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="90196-120">Requirement</span></span> | <span data-ttu-id="90196-121">Valor</span><span class="sxs-lookup"><span data-stu-id="90196-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90196-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90196-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90196-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90196-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="90196-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90196-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90196-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90196-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90196-126">DLL</span><span class="sxs-lookup"><span data-stu-id="90196-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90196-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="90196-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90196-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="90196-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90196-129">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="90196-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="90196-130">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="90196-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





