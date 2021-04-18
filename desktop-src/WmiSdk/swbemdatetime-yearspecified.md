---
description: Valor booliano que indica se o componente de ano no valor de data e hora CIM contém um intervalo ou um valor curinga.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. YearSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3ad6ae5b120c2b38d7b6170951ef30b3b19f5295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760617"
---
# <a name="swbemdatetimeyearspecified-property"></a><span data-ttu-id="bfe1b-103">Propriedade SWbemDateTime. YearSpecified</span><span class="sxs-lookup"><span data-stu-id="bfe1b-103">SWbemDateTime.YearSpecified property</span></span>

<span data-ttu-id="bfe1b-104">A propriedade **YearSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente year no valor DateTime do CIM contém um intervalo ou um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="bfe1b-104">The **YearSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="bfe1b-105">Se **YearSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. Year**](swbemdatetime-year.md) conterá um valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="bfe1b-105">If **YearSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Year**](swbemdatetime-year.md) contains a datetime value.</span></span> <span data-ttu-id="bfe1b-106">Um valor DateTime que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="bfe1b-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="bfe1b-107">Se **YearSpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. Year** conterá um intervalo.</span><span class="sxs-lookup"><span data-stu-id="bfe1b-107">If **YearSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Year** contains an interval.</span></span>

<span data-ttu-id="bfe1b-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bfe1b-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bfe1b-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bfe1b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe1b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfe1b-110">Syntax</span></span>


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bfe1b-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bfe1b-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="bfe1b-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bfe1b-112">Examples</span></span>

<span data-ttu-id="bfe1b-113">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="bfe1b-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="bfe1b-114">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="bfe1b-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe1b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfe1b-115">Requirements</span></span>



| <span data-ttu-id="bfe1b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe1b-116">Requirement</span></span> | <span data-ttu-id="bfe1b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe1b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe1b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfe1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe1b-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfe1b-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfe1b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfe1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe1b-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfe1b-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfe1b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfe1b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe1b-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe1b-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfe1b-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bfe1b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfe1b-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bfe1b-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bfe1b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bfe1b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfe1b-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfe1b-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfe1b-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="bfe1b-128">CLSID</span></span><br/>                    | <span data-ttu-id="bfe1b-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="bfe1b-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="bfe1b-130">IID</span><span class="sxs-lookup"><span data-stu-id="bfe1b-130">IID</span></span><br/>                      | <span data-ttu-id="bfe1b-131">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="bfe1b-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bfe1b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfe1b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe1b-133">**SWbemDateTime. Year**</span><span class="sxs-lookup"><span data-stu-id="bfe1b-133">**SWbemDateTime.Year**</span></span>](swbemdatetime-year.md)
</dt> <dt>

[<span data-ttu-id="bfe1b-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="bfe1b-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="bfe1b-135">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="bfe1b-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




