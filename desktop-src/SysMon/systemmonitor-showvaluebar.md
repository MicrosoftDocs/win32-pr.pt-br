---
title: Propriedade SystemMonitor. ShowValueBar
description: Recupera ou define um valor que determina se a barra de valores (o conjunto de valores estatísticos abaixo do grafo) é exibida no controle.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Propriedade ShowValueBar SysMon
- Propriedade ShowValueBar SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644430"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="d3992-106">Propriedade SystemMonitor. ShowValueBar</span><span class="sxs-lookup"><span data-stu-id="d3992-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="d3992-107">Recupera ou define um valor que determina se a barra de valores (o conjunto de valores estatísticos abaixo do grafo) é exibida no controle.</span><span class="sxs-lookup"><span data-stu-id="d3992-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="d3992-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d3992-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3992-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3992-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d3992-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d3992-110">Property value</span></span>

<span data-ttu-id="d3992-111">Verdadeiro indica que a barra de valores é exibida no controle; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="d3992-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="d3992-112">O valor padrão para essa propriedade é true.</span><span class="sxs-lookup"><span data-stu-id="d3992-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3992-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3992-113">Remarks</span></span>

<span data-ttu-id="d3992-114">As estatísticas exibidas incluem o último valor, o valor médio e os valores mínimo e máximo do contador selecionado no momento durante o intervalo de tempo exibido.</span><span class="sxs-lookup"><span data-stu-id="d3992-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="d3992-115">Para selecionar os valores do contador a serem exibidos, o usuário deve selecionar o contador no painel Legenda do controle.</span><span class="sxs-lookup"><span data-stu-id="d3992-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3992-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3992-116">Requirements</span></span>



| <span data-ttu-id="d3992-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3992-117">Requirement</span></span> | <span data-ttu-id="d3992-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d3992-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3992-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3992-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3992-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3992-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d3992-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3992-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3992-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3992-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3992-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d3992-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3992-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d3992-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3992-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d3992-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3992-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="d3992-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





