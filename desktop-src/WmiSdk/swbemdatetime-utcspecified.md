---
description: Valor booliano que indica se o componente UTC (horário coordenado universal) no valor de data e hora do CIM contém um intervalo ou um valor curinga.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. UTCSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790638"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="2beb4-103">Propriedade SWbemDateTime. UTCSpecified</span><span class="sxs-lookup"><span data-stu-id="2beb4-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="2beb4-104">A propriedade **UTCSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente UTC (horário coordenado universal) no valor DateTime do CIM contém um intervalo ou um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="2beb4-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="2beb4-105">Se **UTCSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. UTC**](swbemdatetime-utc.md) conterá um valor [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="2beb4-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="2beb4-106">Um valor **DateTime** que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="2beb4-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="2beb4-107">Se **UTCSpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. UTC** conterá um intervalo.</span><span class="sxs-lookup"><span data-stu-id="2beb4-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="2beb4-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2beb4-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2beb4-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2beb4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2beb4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2beb4-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="2beb4-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2beb4-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="2beb4-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2beb4-112">Examples</span></span>

<span data-ttu-id="2beb4-113">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="2beb4-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="2beb4-114">Para obter uma descrição do formato de [data e hora CIM, consulte formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="2beb4-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2beb4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2beb4-115">Requirements</span></span>



| <span data-ttu-id="2beb4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2beb4-116">Requirement</span></span> | <span data-ttu-id="2beb4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2beb4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2beb4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2beb4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2beb4-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2beb4-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2beb4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2beb4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2beb4-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2beb4-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2beb4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2beb4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2beb4-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2beb4-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2beb4-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2beb4-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="2beb4-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2beb4-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2beb4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2beb4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2beb4-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2beb4-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2beb4-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="2beb4-128">CLSID</span></span><br/>                    | <span data-ttu-id="2beb4-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="2beb4-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="2beb4-130">IID</span><span class="sxs-lookup"><span data-stu-id="2beb4-130">IID</span></span><br/>                      | <span data-ttu-id="2beb4-131">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="2beb4-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2beb4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="2beb4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beb4-133">**SWbemDateTime. UTC**</span><span class="sxs-lookup"><span data-stu-id="2beb4-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="2beb4-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="2beb4-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="2beb4-135">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="2beb4-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




