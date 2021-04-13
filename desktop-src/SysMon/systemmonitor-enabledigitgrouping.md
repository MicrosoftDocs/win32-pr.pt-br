---
title: Propriedade SystemMonitor. EnableDigitGrouping
description: Recupera ou define um valor que determina se o SYSMON usa o agrupamento de dígitos ao exibir valores numéricos.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propriedade EnableDigitGrouping SysMon
- Propriedade EnableDigitGrouping SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369645"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="0774a-106">Propriedade SystemMonitor. EnableDigitGrouping</span><span class="sxs-lookup"><span data-stu-id="0774a-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="0774a-107">Recupera ou define um valor que determina se o SYSMON usa o agrupamento de dígitos ao exibir valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="0774a-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0774a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0774a-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0774a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0774a-109">Property value</span></span>

<span data-ttu-id="0774a-110">Se for true, o SYSMON agrupará dígitos ao exibir valores numéricos, por exemplo, 1.214.</span><span class="sxs-lookup"><span data-stu-id="0774a-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="0774a-111">Se for false, os valores numéricos não serão agrupados, por exemplo, 1214.</span><span class="sxs-lookup"><span data-stu-id="0774a-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="0774a-112">True é o padrão.</span><span class="sxs-lookup"><span data-stu-id="0774a-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="0774a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0774a-113">Remarks</span></span>

<span data-ttu-id="0774a-114">O símbolo de agrupamento de dígitos está localizado.</span><span class="sxs-lookup"><span data-stu-id="0774a-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0774a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0774a-115">Requirements</span></span>



| <span data-ttu-id="0774a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0774a-116">Requirement</span></span> | <span data-ttu-id="0774a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0774a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0774a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0774a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0774a-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0774a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0774a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0774a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0774a-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0774a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0774a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0774a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0774a-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0774a-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





