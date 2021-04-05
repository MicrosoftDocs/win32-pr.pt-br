---
title: Propriedade SystemMonitor. ReportValueType
description: Recupera ou define um valor que determina se as exibições de histograma e relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado da amostragem, como o valor médio ou mínimo do contador.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Propriedade ReportValueType SysMon
- Propriedade ReportValueType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918407"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="2d7ef-106">Propriedade SystemMonitor. ReportValueType</span><span class="sxs-lookup"><span data-stu-id="2d7ef-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="2d7ef-107">Recupera ou define um valor que determina se as exibições de histograma e relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado da amostragem, como o valor médio ou mínimo do contador.</span><span class="sxs-lookup"><span data-stu-id="2d7ef-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="2d7ef-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2d7ef-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7ef-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d7ef-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="2d7ef-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2d7ef-110">Property value</span></span>

<span data-ttu-id="2d7ef-111">Determina se o histograma e os modos de exibição de relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado a partir do intervalo de amostragem.</span><span class="sxs-lookup"><span data-stu-id="2d7ef-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="2d7ef-112">Para obter os valores possíveis, consulte [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="2d7ef-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d7ef-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d7ef-113">Remarks</span></span>

<span data-ttu-id="2d7ef-114">O SYSMON ignora esse valor e usa [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) não for [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) ou **DisplayTypeConstants.sysmonReport**.</span><span class="sxs-lookup"><span data-stu-id="2d7ef-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d7ef-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d7ef-115">Requirements</span></span>



| <span data-ttu-id="2d7ef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d7ef-116">Requirement</span></span> | <span data-ttu-id="2d7ef-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2d7ef-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7ef-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d7ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d7ef-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2d7ef-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2d7ef-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d7ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d7ef-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2d7ef-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d7ef-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2d7ef-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d7ef-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2d7ef-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d7ef-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d7ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7ef-125">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="2d7ef-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





