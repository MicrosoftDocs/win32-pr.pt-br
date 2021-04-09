---
title: Propriedade SystemMonitor. DisplayType
description: Recupera ou define o tipo de grafo usado para grafar os dados do contador de desempenho.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Propriedade de TipoDeExibição SysMon
- Propriedade doplaytype SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade TipoDeExibição
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085607"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="ee195-106">Propriedade SystemMonitor. DisplayType</span><span class="sxs-lookup"><span data-stu-id="ee195-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="ee195-107">Recupera ou define o tipo de grafo usado para grafar os dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ee195-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="ee195-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ee195-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee195-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee195-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="ee195-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee195-110">Property value</span></span>

<span data-ttu-id="ee195-111">Tipo de grafo usado para grafar os dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ee195-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="ee195-112">Para obter os valores possíveis, consulte [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="ee195-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="ee195-113">Exceções</span><span class="sxs-lookup"><span data-stu-id="ee195-113">Exceptions</span></span>



| <span data-ttu-id="ee195-114">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="ee195-114">Exception type</span></span>               | <span data-ttu-id="ee195-115">Condição</span><span class="sxs-lookup"><span data-stu-id="ee195-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="ee195-116">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="ee195-116">**System.ArgumentException**</span></span> | <span data-ttu-id="ee195-117">O gráfico especificado ou o valor do relatório não é válido.</span><span class="sxs-lookup"><span data-stu-id="ee195-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ee195-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee195-118">Requirements</span></span>



| <span data-ttu-id="ee195-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee195-119">Requirement</span></span> | <span data-ttu-id="ee195-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ee195-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee195-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee195-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee195-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee195-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ee195-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee195-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee195-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee195-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee195-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ee195-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee195-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ee195-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee195-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee195-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee195-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ee195-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





