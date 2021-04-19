---
title: Propriedade SystemMonitor. EnableToolTips
description: Recupera ou define um valor que determina se uma dica de ferramenta é mostrada quando o mouse passa sobre um contador em uma das exibições de gráfico (sem suporte para a exibição de relatório).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Propriedade EnableToolTips SysMon
- Propriedade EnableToolTips SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756531"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="2a3fa-106">Propriedade SystemMonitor. EnableToolTips</span><span class="sxs-lookup"><span data-stu-id="2a3fa-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="2a3fa-107">Recupera ou define um valor que determina se uma dica de ferramenta é mostrada quando o mouse passa sobre um contador em uma das exibições de gráfico (sem suporte para a exibição de relatório).</span><span class="sxs-lookup"><span data-stu-id="2a3fa-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3fa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a3fa-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="2a3fa-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2a3fa-109">Property value</span></span>

<span data-ttu-id="2a3fa-110">Verdadeiro exibe uma dica de ferramenta com as informações do contador; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="2a3fa-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3fa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a3fa-111">Remarks</span></span>

<span data-ttu-id="2a3fa-112">Para grafos de linha, a dica de ferramenta é ancorada ao ponto de dados mais próximo do mouse.</span><span class="sxs-lookup"><span data-stu-id="2a3fa-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="2a3fa-113">Para gráficos de barras e histogramas, a dica de ferramenta representa o valor total de dados da barra, não um ponto dentro da barra.</span><span class="sxs-lookup"><span data-stu-id="2a3fa-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="2a3fa-114">A dica de ferramenta contém informações diferentes com base na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="2a3fa-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="2a3fa-115">Para arquivos de log, a dica de ferramenta contém o caminho do contador, o valor do contador, o carimbo de data/hora, o número de amostras de dados incluídas no ponto de dados e os valores mínimo e máximo de dados.</span><span class="sxs-lookup"><span data-stu-id="2a3fa-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="2a3fa-116">Para a atividade em tempo real, a dica de ferramenta contém o caminho do contador, o valor do contador e o carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="2a3fa-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3fa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a3fa-117">Requirements</span></span>



| <span data-ttu-id="2a3fa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a3fa-118">Requirement</span></span> | <span data-ttu-id="2a3fa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2a3fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3fa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3fa-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a3fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a3fa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3fa-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a3fa-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a3fa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2a3fa-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a3fa-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2a3fa-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





