---
title: Método SystemMonitor BrowseCounters
description: Exibe a caixa de diálogo Adicionar contadores.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Método BrowseCounters SysMon
- Método BrowseCounters SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, método BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008824"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="83303-106">Método SystemMonitor:: BrowseCounters</span><span class="sxs-lookup"><span data-stu-id="83303-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="83303-107">Exibe a caixa de diálogo **Adicionar contadores** .</span><span class="sxs-lookup"><span data-stu-id="83303-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="83303-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83303-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="83303-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83303-109">Parameters</span></span>

<span data-ttu-id="83303-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="83303-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83303-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83303-111">Return value</span></span>

<span data-ttu-id="83303-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="83303-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83303-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="83303-113">Remarks</span></span>

<span data-ttu-id="83303-114">Essa caixa de diálogo permite que o usuário selecione contadores de desempenho locais ou remotos de uma lista de objetos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="83303-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="83303-115">Os contadores selecionados são adicionados à coleção de [**contadores**](counters.md) e exibidos no gráfico ou relatório.</span><span class="sxs-lookup"><span data-stu-id="83303-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="83303-116">Para receber uma notificação quando um contador é adicionado, implemente o evento [**OnCounterAdded**](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="83303-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="83303-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83303-117">Requirements</span></span>



| <span data-ttu-id="83303-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83303-118">Requirement</span></span> | <span data-ttu-id="83303-119">Valor</span><span class="sxs-lookup"><span data-stu-id="83303-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83303-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83303-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83303-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83303-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="83303-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83303-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83303-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83303-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83303-124">DLL</span><span class="sxs-lookup"><span data-stu-id="83303-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83303-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="83303-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83303-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="83303-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83303-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="83303-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="83303-128">**Counters. Add**</span><span class="sxs-lookup"><span data-stu-id="83303-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





