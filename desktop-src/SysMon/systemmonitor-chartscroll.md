---
title: Propriedade SystemMonitor. ChartScroll
description: Recupera ou define um valor que determina se o gráfico de linha rola na exibição.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Propriedade ChartScroll SysMon
- Propriedade ChartScroll SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918551"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="16fe2-106">Propriedade SystemMonitor. ChartScroll</span><span class="sxs-lookup"><span data-stu-id="16fe2-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="16fe2-107">Recupera ou define um valor que determina se o gráfico de linha rola na exibição.</span><span class="sxs-lookup"><span data-stu-id="16fe2-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="16fe2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="16fe2-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="16fe2-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="16fe2-109">Property value</span></span>

<span data-ttu-id="16fe2-110">True se o grafo de linha rolar continuamente da direita para a esquerda; caso contrário, false se o grafo de linha for desenhado da esquerda para a direita e encapsulado sozinho na exibição.</span><span class="sxs-lookup"><span data-stu-id="16fe2-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="16fe2-111">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="16fe2-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="16fe2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="16fe2-112">Remarks</span></span>

<span data-ttu-id="16fe2-113">Esse valor será ignorado se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) não for [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="16fe2-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="16fe2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16fe2-114">Requirements</span></span>



| <span data-ttu-id="16fe2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="16fe2-115">Requirement</span></span> | <span data-ttu-id="16fe2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="16fe2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16fe2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16fe2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16fe2-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16fe2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16fe2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16fe2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16fe2-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16fe2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16fe2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="16fe2-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16fe2-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="16fe2-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





