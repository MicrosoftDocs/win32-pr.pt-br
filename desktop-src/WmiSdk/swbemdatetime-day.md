---
description: Obtém ou define um valor que representa o componente de dia do valor DateTime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Day (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922592"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="59b24-103">Propriedade SWbemDateTime. Day</span><span class="sxs-lookup"><span data-stu-id="59b24-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="59b24-104">A propriedade **Day** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de dia do valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="59b24-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="59b24-105">O valor deve estar no intervalo de 1 a 31 se [**isinterval**](swbemdatetime-isinterval.md) for **false**.</span><span class="sxs-lookup"><span data-stu-id="59b24-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="59b24-106">No entanto, a verificação de erros não é sensível ao valor de mês.</span><span class="sxs-lookup"><span data-stu-id="59b24-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="59b24-107">Assim, o valor de 31 no intervalo não retornará um erro nos casos em que o valor de [**SWbemDateTime. Month**](swbemdatetime-month.md) é de um mês de menos de 31 dias (fevereiro, abril, junho, setembro, novembro).</span><span class="sxs-lookup"><span data-stu-id="59b24-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="59b24-108">O valor padrão para **dia** é 01.</span><span class="sxs-lookup"><span data-stu-id="59b24-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="59b24-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="59b24-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="59b24-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="59b24-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b24-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="59b24-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="59b24-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="59b24-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="59b24-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="59b24-113">Error codes</span></span>

<span data-ttu-id="59b24-114">Depois de obter ou definir a propriedade **Day** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="59b24-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="59b24-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="59b24-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="59b24-116">Se [**isinterval**](swbemdatetime-isinterval.md) for **true** e o intervalo de valores corretos exceder 0 a 99999999.</span><span class="sxs-lookup"><span data-stu-id="59b24-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="59b24-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="59b24-117">Examples</span></span>

<span data-ttu-id="59b24-118">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="59b24-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="59b24-119">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="59b24-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59b24-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b24-120">Requirements</span></span>



| <span data-ttu-id="59b24-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b24-121">Requirement</span></span> | <span data-ttu-id="59b24-122">Valor</span><span class="sxs-lookup"><span data-stu-id="59b24-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59b24-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59b24-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59b24-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59b24-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59b24-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59b24-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59b24-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59b24-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59b24-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59b24-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b24-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b24-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="59b24-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="59b24-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="59b24-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="59b24-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="59b24-131">DLL</span><span class="sxs-lookup"><span data-stu-id="59b24-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59b24-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b24-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="59b24-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="59b24-133">CLSID</span></span><br/>                    | <span data-ttu-id="59b24-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="59b24-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="59b24-135">IID</span><span class="sxs-lookup"><span data-stu-id="59b24-135">IID</span></span><br/>                      | <span data-ttu-id="59b24-136">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="59b24-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="59b24-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="59b24-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b24-138">**SWbemDateTime. DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="59b24-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="59b24-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="59b24-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="59b24-140">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="59b24-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

