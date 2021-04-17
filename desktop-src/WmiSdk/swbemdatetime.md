---
description: O objeto SWbemDateTime é um objeto auxiliar para analisar e definir os valores de data e hora de modelo CIM (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Objeto SWbemDateTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790637"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="a8678-103">Objeto SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a8678-103">SWbemDateTime object</span></span>

<span data-ttu-id="a8678-104">O objeto **SWbemDateTime** é um objeto auxiliar para analisar e definir os valores de [data e hora](datetime.md) de modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="a8678-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="a8678-105">Ele desempenha uma função semelhante a [**SWbemObjectPath**](swbemobjectpath.md), que fornece assistência para formatar e interpretar caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="a8678-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="a8678-106">Você pode usar a chamada do VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) para criar o objeto **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="a8678-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="a8678-107">Um objeto **SWbemDateTime** pode ser inicializado e formatado em um **VT \_ Date** ou em valores **FILETIME** usando métodos no objeto.</span><span class="sxs-lookup"><span data-stu-id="a8678-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="a8678-108">Usando as propriedades do objeto, o valor pode ser analisado no ano do componente, mês, dia, hora, minutos, segundos ou em microssegundos.</span><span class="sxs-lookup"><span data-stu-id="a8678-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="a8678-109">O objeto **SWbemDateTime** pode ser formatado em valores de UTC (tempo Universal local ou coordenado).</span><span class="sxs-lookup"><span data-stu-id="a8678-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="a8678-110">Para obter mais informações, consulte [formato de data e hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a8678-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="a8678-111">**SWbemDateTime** é o único objeto de script Instrumentação de gerenciamento do Windows (WMI) que é marcado como seguro para inicialização e scripts em execução em páginas HTML no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a8678-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="a8678-112">Membros</span><span class="sxs-lookup"><span data-stu-id="a8678-112">Members</span></span>

<span data-ttu-id="a8678-113">O objeto **SWbemDateTime** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a8678-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="a8678-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8678-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8678-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8678-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8678-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8678-116">Methods</span></span>

<span data-ttu-id="a8678-117">O objeto **SWbemDateTime** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a8678-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="a8678-118">Método</span><span class="sxs-lookup"><span data-stu-id="a8678-118">Method</span></span>                                           | <span data-ttu-id="a8678-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8678-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8678-120">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a8678-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="a8678-121">Converte uma data e hora **FILETIME** , expressa como um **BSTR**, em um formato de [data e hora](datetime.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="a8678-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="a8678-122">**GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="a8678-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="a8678-123">Converte um valor de data e hora formatado de [DateTime](datetime.md) do WMI em uma **\_ Data VT**.</span><span class="sxs-lookup"><span data-stu-id="a8678-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="a8678-124">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="a8678-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="a8678-125">Converte um formato de [datahora](datetime.md) WMI em uma data e hora **FILETIME** , expressa como um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a8678-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="a8678-126">**SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="a8678-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="a8678-127">Converte uma data e hora formatadas em **\_ Data VT** em um [DateTime](datetime.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="a8678-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="a8678-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8678-128">Properties</span></span>

<span data-ttu-id="a8678-129">O objeto **SWbemDateTime** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8678-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="a8678-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8678-130">Property</span></span>                                                                        | <span data-ttu-id="a8678-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="a8678-131">Access type</span></span>           | <span data-ttu-id="a8678-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8678-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8678-133">**Dia**</span><span class="sxs-lookup"><span data-stu-id="a8678-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="a8678-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-134">Read/write</span></span><br/> | <span data-ttu-id="a8678-135">O componente de dia de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="a8678-136">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="a8678-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-137">Read/write</span></span><br/> | <span data-ttu-id="a8678-138">Indica se o dia é especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="a8678-139">**Hours**</span><span class="sxs-lookup"><span data-stu-id="a8678-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="a8678-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-140">Read/write</span></span><br/> | <span data-ttu-id="a8678-141">As horas do componente de dia de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="a8678-142">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="a8678-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-143">Read/write</span></span><br/> | <span data-ttu-id="a8678-144">Indica se a hora é especificada ou deixada como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="a8678-145">**Isinterval**</span><span class="sxs-lookup"><span data-stu-id="a8678-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="a8678-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-146">Read/write</span></span><br/> | <span data-ttu-id="a8678-147">Indica que pelo menos um componente do data e [hora](datetime.md) CIM representa um intervalo em vez de uma data.</span><span class="sxs-lookup"><span data-stu-id="a8678-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="a8678-148">**Microssegundos**</span><span class="sxs-lookup"><span data-stu-id="a8678-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="a8678-149">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-149">Read/write</span></span><br/> | <span data-ttu-id="a8678-150">O componente de microssegundos de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="a8678-151">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="a8678-152">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-152">Read/write</span></span><br/> | <span data-ttu-id="a8678-153">Indica se o componente de microssegundos é especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="a8678-154">**minutos**</span><span class="sxs-lookup"><span data-stu-id="a8678-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="a8678-155">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-155">Read/write</span></span><br/> | <span data-ttu-id="a8678-156">O componente de minutos de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="a8678-157">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="a8678-158">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-158">Read/write</span></span><br/> | <span data-ttu-id="a8678-159">Indica se o componente de minutos é especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="a8678-160">**Mês**</span><span class="sxs-lookup"><span data-stu-id="a8678-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="a8678-161">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-161">Read/write</span></span><br/> | <span data-ttu-id="a8678-162">O componente de mês de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="a8678-163">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="a8678-164">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-164">Read/write</span></span><br/> | <span data-ttu-id="a8678-165">Indica se o mês é especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="a8678-166">**Segundos**</span><span class="sxs-lookup"><span data-stu-id="a8678-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="a8678-167">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-167">Read/write</span></span><br/> | <span data-ttu-id="a8678-168">O componente de segundos de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="a8678-169">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="a8678-170">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-170">Read/write</span></span><br/> | <span data-ttu-id="a8678-171">Indica se o componente de segundos é especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="a8678-172">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="a8678-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="a8678-173">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-173">Read/write</span></span><br/> | <span data-ttu-id="a8678-174">O componente UTC de um valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="a8678-175">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="a8678-176">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-176">Read/write</span></span><br/> | <span data-ttu-id="a8678-177">Indica se o componente UTC é especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="a8678-178">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a8678-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="a8678-179">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-179">Read/write</span></span><br/> | <span data-ttu-id="a8678-180">O valor [DateTime](datetime.md) de CIM completo.</span><span class="sxs-lookup"><span data-stu-id="a8678-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="a8678-181">**Year**</span><span class="sxs-lookup"><span data-stu-id="a8678-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="a8678-182">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-182">Read/write</span></span><br/> | <span data-ttu-id="a8678-183">O componente de ano de um valor de [data e hora](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="a8678-184">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="a8678-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="a8678-185">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8678-185">Read/write</span></span><br/> | <span data-ttu-id="a8678-186">Indica se o ano é ou não especificado ou deixado como um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="a8678-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8678-187">Remarks</span></span>

<span data-ttu-id="a8678-188">O WMI registra carimbos de data/hora no formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="a8678-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="a8678-189">O UTC não é o formato que a maioria dos desenvolvedores e administradores de ti usam.</span><span class="sxs-lookup"><span data-stu-id="a8678-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="a8678-190">Portanto, um problema comum é determinar como converter o UTC em algo mais legível.</span><span class="sxs-lookup"><span data-stu-id="a8678-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="a8678-191">Para obter mais informações sobre como trabalhar com o UTC, consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md) e [trabalho com datas e horas usando o WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="a8678-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="a8678-192">Você também pode ler os [s de tempo (Ah, e sobre datas também)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) e [como posso subtrair um número especificado de dias de um valor UTC?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) Postagens de blog para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="a8678-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="a8678-193">Qualquer campo numérico pode ter um valor curinga se a propriedade [**isinterval**](swbemdatetime-isinterval.md) for definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="a8678-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="a8678-194">Os campos com valores curinga contêm asteriscos em todo o campo.</span><span class="sxs-lookup"><span data-stu-id="a8678-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="a8678-195">Cada propriedade, por exemplo, [**Day**](swbemdatetime-day.md), tem um valor booliano especificado correspondente, como [**DaySpecified**](swbemdatetime-dayspecified.md).</span><span class="sxs-lookup"><span data-stu-id="a8678-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="a8678-196">Quando **DaySpecified** é **false**, o valor é interpretado como um intervalo, em vez de um número entre 01 e 31.</span><span class="sxs-lookup"><span data-stu-id="a8678-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="a8678-197">Se um intervalo for usado em qualquer lugar no valor de [data e hora](datetime.md) CIM, [**isinterval**](swbemdatetime-isinterval.md) também será definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a8678-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="a8678-198">O padrão é que um valor DateTime de CIM contenha uma data em vez de um ou mais intervalos.</span><span class="sxs-lookup"><span data-stu-id="a8678-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="a8678-199">Por exemplo, se [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) for **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) incluirá o valor atual de [**SWbemDateTime. Day**](swbemdatetime-day.md), caso contrário, será um valor curinga.</span><span class="sxs-lookup"><span data-stu-id="a8678-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="a8678-200">A propriedade [**isinterval**](swbemdatetime-isinterval.md) é **false** em ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="a8678-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="a8678-201">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8678-201">Examples</span></span>

<span data-ttu-id="a8678-202">O exemplo de código de script a seguir mostra como usar um objeto **SWbemDateTime** para analisar um valor de propriedade DateTime lido no repositório WMI, a propriedade **InstallDate** no sistema [**\_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="a8678-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="a8678-203">O exemplo a seguir mostra como criar um objeto **SWbemDateTime** , armazenar um valor de data no objeto, exibir a data como hora universal local e coordenada (UTC) e armazenar o valor em uma classe e propriedade recém-criadas.</span><span class="sxs-lookup"><span data-stu-id="a8678-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="a8678-204">Para obter mais informações sobre a constante **wbemCimtypeDatetime**, consulte [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="a8678-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="a8678-205">O exemplo de código de script a seguir mostra como usar um objeto **SWbemDateTime** para modificar um valor de intervalo em uma propriedade que é lida no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="a8678-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="a8678-206">O exemplo de código de script a seguir mostra como usar um objeto **SWbemDate** para ler um valor **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="a8678-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="a8678-207">O código do PowerShell a seguir cria uma instância de um objeto SWbemDateTime, recupera a data de instalação do sistema operacional e converte a data em um formato diferente</span><span class="sxs-lookup"><span data-stu-id="a8678-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="a8678-208">O código do PowerShell a seguir converte o código em um formato pronto para ser consumido por um provedor CIM.</span><span class="sxs-lookup"><span data-stu-id="a8678-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="a8678-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8678-209">Requirements</span></span>



| <span data-ttu-id="a8678-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8678-210">Requirement</span></span> | <span data-ttu-id="a8678-211">Valor</span><span class="sxs-lookup"><span data-stu-id="a8678-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8678-212">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8678-212">Minimum supported client</span></span><br/> | <span data-ttu-id="a8678-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8678-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8678-214">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8678-214">Minimum supported server</span></span><br/> | <span data-ttu-id="a8678-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8678-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8678-216">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8678-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8678-217"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8678-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8678-218">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a8678-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8678-219"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8678-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8678-220">DLL</span><span class="sxs-lookup"><span data-stu-id="a8678-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8678-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8678-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8678-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="a8678-222">CLSID</span></span><br/>                    | <span data-ttu-id="a8678-223">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="a8678-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a8678-224">IID</span><span class="sxs-lookup"><span data-stu-id="a8678-224">IID</span></span><br/>                      | <span data-ttu-id="a8678-225">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="a8678-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a8678-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8678-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8678-227">WbemCimtypeEnum</span><span class="sxs-lookup"><span data-stu-id="a8678-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="a8678-228">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="a8678-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="a8678-229">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="a8678-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

