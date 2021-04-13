---
description: Converte uma data no formato de \_ Data VT para o formato de datahora CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetVarDate (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297426"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="5bbb9-103">Método SWbemDateTime. SetVarDate</span><span class="sxs-lookup"><span data-stu-id="5bbb9-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="5bbb9-104">O método **SetVarDate** do objeto [**SWbemDateTime**](swbemdatetime.md) converte uma data no formato de **\_ Data VT** para o formato de [datahora CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbb9-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="5bbb9-105">Um valor de **\_ Data VT** é um valor DateTime de variante que Visual Basic e o uso do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="5bbb9-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5bbb9-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbb9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bbb9-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5bbb9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bbb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbb9-109">*vDate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bbb9-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbb9-110">O valor de data da variante para definir o objeto.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-110">The variant date value to set the object.</span></span> <span data-ttu-id="5bbb9-111">Esse parâmetro deve estar no formato **de \_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="5bbb9-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="5bbb9-112">*bIsLocal* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5bbb9-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbb9-113">Se for **true**, *vDate* será interpretado como uma hora local e a propriedade UTC (tempo Universal Coordenado) conterá a hora local que é convertida no deslocamento UTC correto.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="5bbb9-114">Quando *bIsLocal* é **false**, *vDate* é convertido diretamente em um valor UTC com um deslocamento de zero (0).</span><span class="sxs-lookup"><span data-stu-id="5bbb9-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbb9-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bbb9-115">Return value</span></span>

<span data-ttu-id="5bbb9-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5bbb9-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5bbb9-117">Error codes</span></span>

<span data-ttu-id="5bbb9-118">Depois de concluir o método **SetVarDate** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5bbb9-119">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="5bbb9-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="5bbb9-120">O formato de *vDate* não é válido.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bbb9-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bbb9-121">Remarks</span></span>

<span data-ttu-id="5bbb9-122">Após uma chamada bem-sucedida para **SetVarDate**, o valor [**DateTime**](datetime.md) é interpretado como um valor de DateTime absoluto em vez de um intervalo, e a propriedade [**isinterval**](swbemdatetime-isinterval.md) é definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="5bbb9-123">A função intrínseca Visual Basic ou VBScript [CDATA](/previous-versions//2dt118h2(v=vs.85)) fornece um valor [**DateTime**](datetime.md) no formato **de \_ Data VT** para entrada para **SetVarDate**.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="5bbb9-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bbb9-124">Examples</span></span>

<span data-ttu-id="5bbb9-125">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="5bbb9-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="5bbb9-126">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="5bbb9-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="5bbb9-127">O exemplo de código de [conversão de data para WMI Date-Time formato](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript na galeria do TechNet usa SetVarDate para converter um valor de data e hora regular no formato de data e hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5bbb9-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbb9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bbb9-128">Requirements</span></span>



| <span data-ttu-id="5bbb9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bbb9-129">Requirement</span></span> | <span data-ttu-id="5bbb9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5bbb9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbb9-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bbb9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbb9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bbb9-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5bbb9-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bbb9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbb9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bbb9-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5bbb9-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bbb9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bbb9-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb9-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5bbb9-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5bbb9-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="5bbb9-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb9-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5bbb9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5bbb9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bbb9-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb9-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5bbb9-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="5bbb9-141">CLSID</span></span><br/>                    | <span data-ttu-id="5bbb9-142">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="5bbb9-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="5bbb9-143">IID</span><span class="sxs-lookup"><span data-stu-id="5bbb9-143">IID</span></span><br/>                      | <span data-ttu-id="5bbb9-144">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="5bbb9-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5bbb9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bbb9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbb9-146">**SWbemDateTime. SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="5bbb9-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="5bbb9-147">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5bbb9-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="5bbb9-148">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="5bbb9-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

