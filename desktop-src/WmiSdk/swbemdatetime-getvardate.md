---
description: Converte um valor de data e hora no formato CIM DATETIME no formato de \_ Data VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Método SWbemDateTime. GetVarDate (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814429"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="a290a-103">Método SWbemDateTime. GetVarDate</span><span class="sxs-lookup"><span data-stu-id="a290a-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="a290a-104">O método **GetVarDate** do objeto [**SWbemDateTime**](swbemdatetime.md) converte um valor de data e hora no formato CIM [**DateTime**](datetime.md) no formato de **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="a290a-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="a290a-105">O formato de **\_ Data VT** é um valor [**DateTime**](datetime.md) de variante de automação que Visual Basic e o uso do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a290a-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="a290a-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a290a-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a290a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a290a-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a290a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a290a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a290a-109">*bIsLocal* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a290a-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a290a-110">Indica se o valor retornado é interpretado como hora local.</span><span class="sxs-lookup"><span data-stu-id="a290a-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="a290a-111">A propriedade UTC (tempo Universal Coordenado) contém a hora local convertida para o deslocamento UTC correto.</span><span class="sxs-lookup"><span data-stu-id="a290a-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="a290a-112">Se o valor for **false**, o valor será interpretado como UTC com um deslocamento zero (0).</span><span class="sxs-lookup"><span data-stu-id="a290a-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a290a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a290a-113">Return value</span></span>

<span data-ttu-id="a290a-114">O valor de data e hora no formato de **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="a290a-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="a290a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a290a-115">Remarks</span></span>

<span data-ttu-id="a290a-116">**VT \_** Os valores de data e **FILETIME** não podem conter campos curinga.</span><span class="sxs-lookup"><span data-stu-id="a290a-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="a290a-117">O método **GetVarDate** falhará (**wbemErrFailed**) se qualquer uma das seguintes propriedades for **falsa**:</span><span class="sxs-lookup"><span data-stu-id="a290a-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="a290a-118">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="a290a-119">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="a290a-120">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="a290a-121">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="a290a-122">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="a290a-123">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="a290a-124">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="a290a-125">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="a290a-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="a290a-126">Após o retorno bem-sucedido de [**SetVarDate**](swbemdatetime-setvardate.md), todas essas propriedades são definidas como **true**.</span><span class="sxs-lookup"><span data-stu-id="a290a-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="a290a-127">Após uma chamada bem-sucedida para [**SetVarDate**](swbemdatetime-setvardate.md), o valor [**DateTime**](datetime.md) é sempre interpretado como um valor **DateTime** absoluto, em vez de um intervalo, e o [**isinterval**](swbemdatetime-isinterval.md) é definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="a290a-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="a290a-128">Se [**isinterval**](swbemdatetime-isinterval.md) for definido como **true**, uma chamada para **GetVarDate** resultará no erro **wbemErrFailed** .</span><span class="sxs-lookup"><span data-stu-id="a290a-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="a290a-129">Uma perda de precisão ocorre quando você chama **GetVarDate**, pois os valores de [DateTime](datetime.md) têm uma resolução de um microssegundo (s) e os valores de **\_ data VT** têm uma resolução de 500 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a290a-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="a290a-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a290a-130">Examples</span></span>

<span data-ttu-id="a290a-131">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM para e do formato de **\_ dados** **FILETIME** ou VT, consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="a290a-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="a290a-132">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a290a-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a290a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a290a-133">Requirements</span></span>



| <span data-ttu-id="a290a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a290a-134">Requirement</span></span> | <span data-ttu-id="a290a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a290a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a290a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a290a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a290a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a290a-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a290a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a290a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a290a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a290a-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a290a-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a290a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a290a-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a290a-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a290a-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a290a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="a290a-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a290a-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a290a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a290a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a290a-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a290a-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a290a-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="a290a-146">CLSID</span></span><br/>                    | <span data-ttu-id="a290a-147">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="a290a-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a290a-148">IID</span><span class="sxs-lookup"><span data-stu-id="a290a-148">IID</span></span><br/>                      | <span data-ttu-id="a290a-149">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="a290a-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a290a-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a290a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a290a-151">**SWbemDateTime. GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a290a-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="a290a-152">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a290a-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="a290a-153">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="a290a-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




