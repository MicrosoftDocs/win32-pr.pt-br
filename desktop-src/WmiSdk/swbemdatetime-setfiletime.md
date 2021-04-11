---
description: Converte uma data no formato FILETIME da cadeia de caracteres para o formato de data e hora CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetFileTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091293"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="b0e2e-103">Método SWbemDateTime. SetFileTime</span><span class="sxs-lookup"><span data-stu-id="b0e2e-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="b0e2e-104">O método **SetFileTime** do objeto [**SWbemDateTime**](swbemdatetime.md) converte uma data no formato **FILETIME** da cadeia de caracteres para o formato de [data e hora CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e2e-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="b0e2e-105">O formato **FILETIME** é uma estrutura datetime de 64 bits que representa o número de unidades de 100 nanossegundos desde o início de 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="b0e2e-106">Instrumentação de Gerenciamento do Windows (WMI) trata os valores de **FILETIME** como representações de cadeia de caracteres de números de 64 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="b0e2e-107">Para obter a explicação da sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b0e2e-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e2e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0e2e-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b0e2e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0e2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e2e-110">*strFileTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0e2e-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e2e-111">Valor **FILETIME** usado para definir o objeto.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="b0e2e-112">*bIsLocal* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0e2e-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e2e-113">Se for **true**, *strFileTime* será interpretado como uma hora local.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="b0e2e-114">A propriedade UTC (tempo Universal Coordenado) contém a hora local convertida para o deslocamento UTC correto.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="b0e2e-115">Quando *bIsLocal* é **false**, *strFileTime* é convertido diretamente em um valor UTC com um deslocamento de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b0e2e-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e2e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0e2e-116">Return value</span></span>

<span data-ttu-id="b0e2e-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0e2e-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b0e2e-118">Error codes</span></span>

<span data-ttu-id="b0e2e-119">Depois de concluir o método **SetFileTime** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b0e2e-120">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="b0e2e-121">O formato de *strFileTime* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0e2e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0e2e-122">Remarks</span></span>

<span data-ttu-id="b0e2e-123">Após uma chamada bem-sucedida para **SetFileTime**, o valor [**DateTime**](datetime.md) é sempre interpretado como um valor absoluto (**DateTime**) e [**isinterval**](swbemdatetime-isinterval.md) é definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="b0e2e-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0e2e-124">Examples</span></span>

<span data-ttu-id="b0e2e-125">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="b0e2e-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="b0e2e-126">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="b0e2e-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e2e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0e2e-127">Requirements</span></span>



| <span data-ttu-id="b0e2e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0e2e-128">Requirement</span></span> | <span data-ttu-id="b0e2e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b0e2e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e2e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0e2e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e2e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0e2e-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0e2e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0e2e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e2e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0e2e-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0e2e-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0e2e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e2e-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e2e-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0e2e-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b0e2e-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0e2e-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b0e2e-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b0e2e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b0e2e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0e2e-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0e2e-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b0e2e-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="b0e2e-140">CLSID</span></span><br/>                    | <span data-ttu-id="b0e2e-141">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="b0e2e-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="b0e2e-142">IID</span><span class="sxs-lookup"><span data-stu-id="b0e2e-142">IID</span></span><br/>                      | <span data-ttu-id="b0e2e-143">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="b0e2e-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b0e2e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0e2e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e2e-145">**SWbemDateTime. SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="b0e2e-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="b0e2e-146">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="b0e2e-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="b0e2e-147">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="b0e2e-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

