---
title: Propriedade SystemMonitor. Highlight
description: Recupera ou define um valor que indica se os valores dos contadores selecionados são realçados no grafo.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Realçar a propriedade SysMon
- Realçar a propriedade SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade de realce
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824430"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="6a119-106">Propriedade SystemMonitor. Highlight</span><span class="sxs-lookup"><span data-stu-id="6a119-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="6a119-107">Recupera ou define um valor que indica se os valores dos contadores selecionados são realçados no grafo.</span><span class="sxs-lookup"><span data-stu-id="6a119-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="6a119-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6a119-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a119-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a119-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6a119-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6a119-110">Property value</span></span>

<span data-ttu-id="6a119-111">Verdadeiro indica que os valores dos contadores selecionados são realçados no grafo; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="6a119-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="6a119-112">O valor padrão é False.</span><span class="sxs-lookup"><span data-stu-id="6a119-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a119-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a119-113">Remarks</span></span>

<span data-ttu-id="6a119-114">Para selecionar um ou mais contadores, você pode definir [**MyItem. Selected**](counteritem-selected.md) como true ou o usuário pode selecionar os contadores na lista de contadores mostrados na legenda.</span><span class="sxs-lookup"><span data-stu-id="6a119-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="6a119-115">**Antes do Windows Vista:** Não é possível selecionar contadores de forma programática e o usuário pode selecionar apenas um contador na lista de contadores mostrados na legenda.</span><span class="sxs-lookup"><span data-stu-id="6a119-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="6a119-116">O realce pode ser preto ou branco, dependendo do valor da propriedade [**BackColor**](systemmonitor-backcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="6a119-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="6a119-117">O realce é definido automaticamente com a cor que fornecerá contraste suficiente entre a cor de realce e a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6a119-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a119-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a119-118">Requirements</span></span>



| <span data-ttu-id="6a119-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a119-119">Requirement</span></span> | <span data-ttu-id="6a119-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6a119-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a119-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a119-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a119-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a119-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6a119-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a119-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a119-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a119-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a119-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a119-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a119-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6a119-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a119-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6a119-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a119-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6a119-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="6a119-129">**Coitem. selecionado**</span><span class="sxs-lookup"><span data-stu-id="6a119-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





