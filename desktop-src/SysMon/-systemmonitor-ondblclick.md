---
title: Evento SystemMonitor. AoClicarDuasVezes
description: Notifica quando um usuário clica duas vezes na linha do gráfico, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento de AoClicarDuasVezes do SysMon
- Evento AoClicarDuasVezes SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento AoClicarDuasVezes
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085608"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="6fd08-106">Evento SystemMonitor. AoClicarDuasVezes</span><span class="sxs-lookup"><span data-stu-id="6fd08-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="6fd08-107">Notifica quando um usuário clica duas vezes na linha do gráfico, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="6fd08-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd08-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fd08-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="6fd08-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fd08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd08-110">*índice* \[ do entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6fd08-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd08-111">Índice do contador selecionado no objeto da coleção de [**contadores**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd08-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="6fd08-112">Um valor de índice 0 será retornado se nenhum contador tiver sido selecionado; caso contrário, o índice do contador selecionado será retornado.</span><span class="sxs-lookup"><span data-stu-id="6fd08-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd08-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fd08-113">Return value</span></span>

<span data-ttu-id="6fd08-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6fd08-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd08-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fd08-115">Remarks</span></span>

<span data-ttu-id="6fd08-116">Quando esse evento é disparado, o contador que o usuário selecionou no grafo de linha e no histograma também é selecionado no painel Legenda.</span><span class="sxs-lookup"><span data-stu-id="6fd08-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="6fd08-117">Isso torna mais fácil para o usuário do monitor do sistema ver qual contador é selecionado quando vários valores de contador são exibidos.</span><span class="sxs-lookup"><span data-stu-id="6fd08-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd08-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fd08-118">Requirements</span></span>



| <span data-ttu-id="6fd08-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd08-119">Requirement</span></span> | <span data-ttu-id="6fd08-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6fd08-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd08-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fd08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd08-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fd08-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6fd08-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fd08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd08-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fd08-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fd08-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd08-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd08-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6fd08-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





