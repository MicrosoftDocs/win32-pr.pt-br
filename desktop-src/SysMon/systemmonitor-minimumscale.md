---
title: Propriedade SystemMonitor. MinimumScale
description: Recupera ou define o valor mínimo do eixo vertical (Y) do grafo.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Propriedade MinimumScale SysMon
- Propriedade MinimumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455099"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="49374-106">Propriedade SystemMonitor. MinimumScale</span><span class="sxs-lookup"><span data-stu-id="49374-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="49374-107">Recupera ou define o valor mínimo do eixo vertical (Y) do grafo.</span><span class="sxs-lookup"><span data-stu-id="49374-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="49374-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="49374-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49374-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49374-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="49374-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="49374-110">Property value</span></span>

<span data-ttu-id="49374-111">Valor mínimo positivo do eixo vertical do grafo.</span><span class="sxs-lookup"><span data-stu-id="49374-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="49374-112">O valor mínimo padrão da escala vertical é 0.</span><span class="sxs-lookup"><span data-stu-id="49374-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="49374-113">O valor mais alto para o qual você pode definir o valor mínimo é um valor menor que [**MaximumScale**](systemmonitor-maximumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="49374-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49374-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="49374-114">Remarks</span></span>

<span data-ttu-id="49374-115">O controle ajusta automaticamente a posição dos números de escala exibidos na escala vertical de acordo com o tamanho do controle exibido.</span><span class="sxs-lookup"><span data-stu-id="49374-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="49374-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49374-116">Requirements</span></span>



| <span data-ttu-id="49374-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="49374-117">Requirement</span></span> | <span data-ttu-id="49374-118">Valor</span><span class="sxs-lookup"><span data-stu-id="49374-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49374-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49374-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49374-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49374-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="49374-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49374-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49374-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49374-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49374-123">DLL</span><span class="sxs-lookup"><span data-stu-id="49374-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49374-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="49374-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49374-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="49374-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49374-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="49374-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="49374-127">**SystemMonitor.MaximumScale**</span><span class="sxs-lookup"><span data-stu-id="49374-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="49374-128">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="49374-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





