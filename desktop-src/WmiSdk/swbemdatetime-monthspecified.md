---
description: Valor booliano que indica se o componente de mês no valor de data e hora CIM contém um intervalo ou um valor curinga.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. MonthSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797626"
---
# <a name="swbemdatetimemonthspecified-property"></a><span data-ttu-id="6ee48-103">Propriedade SWbemDateTime. MonthSpecified</span><span class="sxs-lookup"><span data-stu-id="6ee48-103">SWbemDateTime.MonthSpecified property</span></span>

<span data-ttu-id="6ee48-104">A propriedade **MonthSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente de mês no valor DateTime do CIM contém um intervalo ou um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="6ee48-104">The **MonthSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="6ee48-105">Se **MonthSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. Month**](swbemdatetime-month.md) conterá um valor Date.</span><span class="sxs-lookup"><span data-stu-id="6ee48-105">If **MonthSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Month**](swbemdatetime-month.md) contains a date value.</span></span> <span data-ttu-id="6ee48-106">Um valor DateTime que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="6ee48-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="6ee48-107">Se **MonthSpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. Month** conterá um intervalo.</span><span class="sxs-lookup"><span data-stu-id="6ee48-107">If **MonthSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Month** contains an interval.</span></span>

<span data-ttu-id="6ee48-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6ee48-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6ee48-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6ee48-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee48-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ee48-110">Syntax</span></span>


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6ee48-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6ee48-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6ee48-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6ee48-112">Examples</span></span>

<span data-ttu-id="6ee48-113">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="6ee48-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="6ee48-114">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="6ee48-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee48-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee48-115">Requirements</span></span>



| <span data-ttu-id="6ee48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee48-116">Requirement</span></span> | <span data-ttu-id="6ee48-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee48-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee48-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ee48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee48-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ee48-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ee48-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ee48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee48-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ee48-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ee48-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ee48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee48-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee48-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ee48-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ee48-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ee48-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ee48-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ee48-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee48-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee48-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ee48-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ee48-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="6ee48-128">CLSID</span></span><br/>                    | <span data-ttu-id="6ee48-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="6ee48-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6ee48-130">IID</span><span class="sxs-lookup"><span data-stu-id="6ee48-130">IID</span></span><br/>                      | <span data-ttu-id="6ee48-131">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="6ee48-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6ee48-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ee48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee48-133">**SWbemDateTime. Month**</span><span class="sxs-lookup"><span data-stu-id="6ee48-133">**SWbemDateTime.Month**</span></span>](swbemdatetime-month.md)
</dt> <dt>

[<span data-ttu-id="6ee48-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="6ee48-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="6ee48-135">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="6ee48-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




