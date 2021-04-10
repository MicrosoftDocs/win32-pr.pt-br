---
description: Indica se o componente de minutos no valor de data e hora CIM contém um intervalo ou um valor curinga.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. MinutesSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091294"
---
# <a name="swbemdatetimeminutesspecified-property"></a><span data-ttu-id="82603-103">Propriedade SWbemDateTime. MinutesSpecified</span><span class="sxs-lookup"><span data-stu-id="82603-103">SWbemDateTime.MinutesSpecified property</span></span>

<span data-ttu-id="82603-104">A propriedade **MinutesSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente de minutos no valor DateTime do CIM contém um intervalo ou um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="82603-104">The **MinutesSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="82603-105">Se **MinutesSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false** (indicando que o valor de DateTime de CIM não tem curingas), então [**SWbemDateTime. Minutes**](swbemdatetime-minutes.md) contém um valor de data.</span><span class="sxs-lookup"><span data-stu-id="82603-105">If **MinutesSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE** (indicating that the CIM datetime value has no wildcards), then [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contains a date value.</span></span> <span data-ttu-id="82603-106">Um valor DateTime que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="82603-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="82603-107">Se [**HoursSpecified**](swbemdatetime-hoursspecified.md) for **false** e **isinterval** for **true**, **SWbemDateTime. Minutes** conterá um intervalo.</span><span class="sxs-lookup"><span data-stu-id="82603-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Minutes** contains an interval.</span></span>

<span data-ttu-id="82603-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="82603-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="82603-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="82603-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="82603-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="82603-110">Syntax</span></span>


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a><span data-ttu-id="82603-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="82603-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="82603-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82603-112">Examples</span></span>

<span data-ttu-id="82603-113">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="82603-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="82603-114">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="82603-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82603-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82603-115">Requirements</span></span>



| <span data-ttu-id="82603-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="82603-116">Requirement</span></span> | <span data-ttu-id="82603-117">Valor</span><span class="sxs-lookup"><span data-stu-id="82603-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82603-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82603-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82603-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82603-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82603-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82603-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82603-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82603-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82603-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82603-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="82603-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="82603-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="82603-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="82603-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="82603-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82603-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82603-126">DLL</span><span class="sxs-lookup"><span data-stu-id="82603-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82603-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82603-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="82603-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="82603-128">CLSID</span></span><br/>                    | <span data-ttu-id="82603-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="82603-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="82603-130">IID</span><span class="sxs-lookup"><span data-stu-id="82603-130">IID</span></span><br/>                      | <span data-ttu-id="82603-131">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="82603-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="82603-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="82603-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82603-133">**SWbemDateTime. minutos**</span><span class="sxs-lookup"><span data-stu-id="82603-133">**SWbemDateTime.Minutes**</span></span>](swbemdatetime-minutes.md)
</dt> <dt>

[<span data-ttu-id="82603-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="82603-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="82603-135">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="82603-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




