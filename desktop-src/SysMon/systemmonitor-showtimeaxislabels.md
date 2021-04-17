---
title: Propriedade SystemMonitor. ShowTimeAxisLabels
description: Recupera ou define um valor que determina se o eixo horizontal (X) da exibição de gráfico contém rótulos.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Propriedade ShowTimeAxisLabels SysMon
- Propriedade ShowTimeAxisLabels SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749185"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="77146-106">Propriedade SystemMonitor. ShowTimeAxisLabels</span><span class="sxs-lookup"><span data-stu-id="77146-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="77146-107">Recupera ou define um valor que determina se o eixo horizontal (X) da exibição de gráfico contém rótulos.</span><span class="sxs-lookup"><span data-stu-id="77146-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="77146-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="77146-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="77146-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="77146-109">Property value</span></span>

<span data-ttu-id="77146-110">Um valor true aplicará rótulos ao eixo x.</span><span class="sxs-lookup"><span data-stu-id="77146-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="77146-111">Um valor false não será.</span><span class="sxs-lookup"><span data-stu-id="77146-111">A value of False will not.</span></span> <span data-ttu-id="77146-112">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="77146-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="77146-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="77146-113">Remarks</span></span>

<span data-ttu-id="77146-114">O SYSMON ignora essa propriedade para gráficos de barras, relatórios e histogramas.</span><span class="sxs-lookup"><span data-stu-id="77146-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="77146-115">Para grafos de linha, o SYSMON usa a hora em que o valor do contador foi amostrado como o rótulo.</span><span class="sxs-lookup"><span data-stu-id="77146-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="77146-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77146-116">Requirements</span></span>



| <span data-ttu-id="77146-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77146-117">Requirement</span></span> | <span data-ttu-id="77146-118">Valor</span><span class="sxs-lookup"><span data-stu-id="77146-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77146-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77146-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77146-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77146-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77146-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77146-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77146-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77146-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77146-123">DLL</span><span class="sxs-lookup"><span data-stu-id="77146-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77146-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="77146-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





