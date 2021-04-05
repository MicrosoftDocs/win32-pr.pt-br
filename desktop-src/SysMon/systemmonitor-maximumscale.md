---
title: Propriedade SystemMonitor. MaximumScale
description: Recupera ou define o valor máximo do eixo vertical (Y) do grafo.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Propriedade MaximumScale SysMon
- Propriedade MaximumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918316"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="3ffd8-106">Propriedade SystemMonitor. MaximumScale</span><span class="sxs-lookup"><span data-stu-id="3ffd8-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="3ffd8-107">Recupera ou define o valor máximo do eixo vertical (Y) do grafo.</span><span class="sxs-lookup"><span data-stu-id="3ffd8-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="3ffd8-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3ffd8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffd8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ffd8-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="3ffd8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3ffd8-110">Property value</span></span>

<span data-ttu-id="3ffd8-111">Valor máximo positivo do eixo vertical do grafo.</span><span class="sxs-lookup"><span data-stu-id="3ffd8-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="3ffd8-112">O valor máximo padrão da escala vertical é 100.</span><span class="sxs-lookup"><span data-stu-id="3ffd8-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="3ffd8-113">O menor valor para o qual você pode definir o valor máximo é mais do que o valor de [**MinimumScale**](systemmonitor-minimumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="3ffd8-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="3ffd8-114">O valor mais alto para o qual você pode definir o valor máximo é 999.999.999.</span><span class="sxs-lookup"><span data-stu-id="3ffd8-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ffd8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ffd8-115">Remarks</span></span>

<span data-ttu-id="3ffd8-116">O controle ajusta automaticamente a posição dos números de escala exibidos na escala vertical de acordo com o tamanho do controle exibido.</span><span class="sxs-lookup"><span data-stu-id="3ffd8-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ffd8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ffd8-117">Requirements</span></span>



| <span data-ttu-id="3ffd8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ffd8-118">Requirement</span></span> | <span data-ttu-id="3ffd8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffd8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffd8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ffd8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffd8-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ffd8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3ffd8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ffd8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffd8-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ffd8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ffd8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3ffd8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ffd8-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3ffd8-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ffd8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ffd8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffd8-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3ffd8-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="3ffd8-128">**SystemMonitor.MinimumScale**</span><span class="sxs-lookup"><span data-stu-id="3ffd8-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="3ffd8-129">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="3ffd8-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





