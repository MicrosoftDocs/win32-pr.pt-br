---
description: Valor booliano que indica se o componente de segundos no valor de data e hora CIM contém um intervalo ou um valor curinga.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. SecondsSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837074"
---
# <a name="swbemdatetimesecondsspecified-property"></a><span data-ttu-id="f2086-103">Propriedade SWbemDateTime. SecondsSpecified</span><span class="sxs-lookup"><span data-stu-id="f2086-103">SWbemDateTime.SecondsSpecified property</span></span>

<span data-ttu-id="f2086-104">A propriedade **SecondsSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente de segundos no valor [**DateTime**](datetime.md) do CIM contém um intervalo ou um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="f2086-104">The **SecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the seconds component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="f2086-105">Se **SecondsSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. Seconds**](swbemdatetime-seconds.md) conterá um valor Date.</span><span class="sxs-lookup"><span data-stu-id="f2086-105">If **SecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contains a date value.</span></span> <span data-ttu-id="f2086-106">Um valor DateTime que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="f2086-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="f2086-107">Se **SecondsSpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. Seconds** conterá um intervalo.</span><span class="sxs-lookup"><span data-stu-id="f2086-107">If **SecondsSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Seconds** contains an interval.</span></span>

<span data-ttu-id="f2086-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2086-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f2086-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f2086-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2086-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2086-110">Syntax</span></span>


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f2086-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f2086-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="f2086-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2086-112">Examples</span></span>

<span data-ttu-id="f2086-113">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="f2086-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f2086-114">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="f2086-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2086-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2086-115">Requirements</span></span>



| <span data-ttu-id="f2086-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2086-116">Requirement</span></span> | <span data-ttu-id="f2086-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f2086-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2086-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2086-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2086-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2086-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2086-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2086-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2086-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2086-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2086-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2086-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2086-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2086-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2086-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f2086-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2086-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2086-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2086-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f2086-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2086-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2086-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2086-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2086-128">CLSID</span></span><br/>                    | <span data-ttu-id="f2086-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="f2086-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f2086-130">IID</span><span class="sxs-lookup"><span data-stu-id="f2086-130">IID</span></span><br/>                      | <span data-ttu-id="f2086-131">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="f2086-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f2086-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2086-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2086-133">**SWbemDateTime. segundos**</span><span class="sxs-lookup"><span data-stu-id="f2086-133">**SWbemDateTime.Seconds**</span></span>](swbemdatetime-seconds.md)
</dt> <dt>

[<span data-ttu-id="f2086-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f2086-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f2086-135">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="f2086-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




