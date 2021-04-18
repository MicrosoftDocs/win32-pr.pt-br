---
description: Valor booliano que indica se o componente de dia no valor de data e hora CIM contém um intervalo ou um valor curinga.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. DaySpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788636"
---
# <a name="swbemdatetimedayspecified-property"></a><span data-ttu-id="5587f-103">Propriedade SWbemDateTime. DaySpecified</span><span class="sxs-lookup"><span data-stu-id="5587f-103">SWbemDateTime.DaySpecified property</span></span>

<span data-ttu-id="5587f-104">A propriedade **DaySpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente de dia no valor [**DateTime**](datetime.md) do CIM contém um intervalo ou um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="5587f-104">The **DaySpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the day component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="5587f-105">Se **DaySpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. Day**](swbemdatetime-day.md) conterá um valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="5587f-105">If **DaySpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Day**](swbemdatetime-day.md) contains a datetime value.</span></span> <span data-ttu-id="5587f-106">Um valor [**DateTime**](datetime.md) que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="5587f-106">A [**DATETIME**](datetime.md) value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="5587f-107">Se **DaySpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. Day** conterá um intervalo.</span><span class="sxs-lookup"><span data-stu-id="5587f-107">If **DaySpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Day** contains an interval.</span></span>

<span data-ttu-id="5587f-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5587f-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5587f-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5587f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5587f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5587f-110">Syntax</span></span>


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="5587f-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5587f-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="5587f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5587f-112">Examples</span></span>

<span data-ttu-id="5587f-113">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="5587f-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="5587f-114">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="5587f-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5587f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5587f-115">Requirements</span></span>



| <span data-ttu-id="5587f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5587f-116">Requirement</span></span> | <span data-ttu-id="5587f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5587f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5587f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5587f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5587f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5587f-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5587f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5587f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5587f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5587f-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5587f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5587f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5587f-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5587f-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5587f-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5587f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5587f-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5587f-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5587f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5587f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5587f-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5587f-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5587f-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="5587f-128">CLSID</span></span><br/>                    | <span data-ttu-id="5587f-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="5587f-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="5587f-130">IID</span><span class="sxs-lookup"><span data-stu-id="5587f-130">IID</span></span><br/>                      | <span data-ttu-id="5587f-131">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="5587f-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5587f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5587f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5587f-133">**SWbemDateTime. Day**</span><span class="sxs-lookup"><span data-stu-id="5587f-133">**SWbemDateTime.Day**</span></span>](swbemdatetime-day.md)
</dt> <dt>

[<span data-ttu-id="5587f-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5587f-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="5587f-135">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="5587f-135">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




