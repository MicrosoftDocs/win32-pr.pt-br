---
description: Converte um valor de data e hora no formato de datahora CIM no formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Método SWbemDateTime. GetFileTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461312"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="40349-103">Método SWbemDateTime. GetFileTime</span><span class="sxs-lookup"><span data-stu-id="40349-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="40349-104">O método **GetFileTime** do objeto [**SWbemDateTime**](swbemdatetime.md) converte um valor de data e hora no formato de [DateTime](datetime.md) do CIM para o formato FILETIME.</span><span class="sxs-lookup"><span data-stu-id="40349-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="40349-105">Se o parâmetro for definido como **true**, o valor de retorno representará uma hora local para o cliente.</span><span class="sxs-lookup"><span data-stu-id="40349-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="40349-106">Caso contrário, o valor de retorno será uma hora UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="40349-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="40349-107">Uma estrutura de [data e hora](datetime.md) **FILETIME** é um valor de 64 bits que representa o número de unidades de 100 nanossegundos desde o início de 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="40349-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="40349-108">Instrumentação de Gerenciamento do Windows (WMI) trata os valores de **FILETIME** como representações de cadeia de caracteres de números de 64 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="40349-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="40349-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="40349-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40349-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40349-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="40349-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40349-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40349-112">*bIsLocaL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="40349-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="40349-113">Indica se o valor retornado é interpretado como hora local.</span><span class="sxs-lookup"><span data-stu-id="40349-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="40349-114">A propriedade UTC então contém a hora local convertida no deslocamento UTC (tempo Universal Coordenado) correto.</span><span class="sxs-lookup"><span data-stu-id="40349-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="40349-115">Se o valor for **false**, o valor será interpretado como UTC com um deslocamento zero (0).</span><span class="sxs-lookup"><span data-stu-id="40349-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40349-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40349-116">Return value</span></span>

<span data-ttu-id="40349-117">A data e a hora no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="40349-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40349-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="40349-118">Error codes</span></span>

<span data-ttu-id="40349-119">Depois de concluir o método **GetFileTime** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="40349-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="40349-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="40349-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="40349-121">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="40349-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40349-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="40349-122">Remarks</span></span>

<span data-ttu-id="40349-123">**VT \_** Os valores de data e **FILETIME** não podem conter campos curinga.</span><span class="sxs-lookup"><span data-stu-id="40349-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="40349-124">O método **filefiletime** falhará (wbemErrFailed) se qualquer uma das seguintes propriedades for **false**:</span><span class="sxs-lookup"><span data-stu-id="40349-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="40349-125">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="40349-126">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="40349-127">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="40349-128">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="40349-129">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="40349-130">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="40349-131">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="40349-132">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="40349-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="40349-133">Em um retorno bem-sucedido de [**SetFileTime**](swbemdatetime-setfiletime.md), todas essas propriedades são definidas como **true**.</span><span class="sxs-lookup"><span data-stu-id="40349-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="40349-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40349-134">Examples</span></span>

<span data-ttu-id="40349-135">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="40349-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="40349-136">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="40349-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40349-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40349-137">Requirements</span></span>



| <span data-ttu-id="40349-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="40349-138">Requirement</span></span> | <span data-ttu-id="40349-139">Valor</span><span class="sxs-lookup"><span data-stu-id="40349-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40349-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40349-140">Minimum supported client</span></span><br/> | <span data-ttu-id="40349-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40349-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40349-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40349-142">Minimum supported server</span></span><br/> | <span data-ttu-id="40349-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40349-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40349-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40349-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="40349-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40349-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40349-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="40349-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="40349-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40349-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40349-148">DLL</span><span class="sxs-lookup"><span data-stu-id="40349-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40349-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40349-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="40349-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="40349-150">CLSID</span></span><br/>                    | <span data-ttu-id="40349-151">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="40349-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="40349-152">IID</span><span class="sxs-lookup"><span data-stu-id="40349-152">IID</span></span><br/>                      | <span data-ttu-id="40349-153">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="40349-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="40349-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="40349-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40349-155">**SWbemDateTime. GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="40349-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="40349-156">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="40349-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="40349-157">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="40349-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

