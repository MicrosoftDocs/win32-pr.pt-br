---
description: Obtém ou define um valor que representa o componente de minutos do valor DateTime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Minutes (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763301"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="a96a3-103">Propriedade SWbemDateTime. Minutes</span><span class="sxs-lookup"><span data-stu-id="a96a3-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="a96a3-104">A propriedade **minutes** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de minutos do valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="a96a3-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="a96a3-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a96a3-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a96a3-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a96a3-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a96a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a96a3-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="a96a3-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a96a3-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="a96a3-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a96a3-109">Error codes</span></span>

<span data-ttu-id="a96a3-110">Depois de obter ou definir a propriedade **minutes** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="a96a3-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="a96a3-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="a96a3-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="a96a3-112">O valor não estava no intervalo de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="a96a3-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a96a3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a96a3-113">Remarks</span></span>

<span data-ttu-id="a96a3-114">Se a propriedade **SWbemDateTime. Minutes** for definida como 1, a propriedade [**SWbemDateTime. Seconds**](swbemdatetime-seconds.md) conterá um valor que é deslocado por um segundo um erro de arredondamento que ocorre quando um valor **DateTime** de CIM é convertido em um valor de **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="a96a3-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="a96a3-115">Se a propriedade **minutes** for definida como 0 em vez disso, a propriedade **Seconds** retornará o valor correto.</span><span class="sxs-lookup"><span data-stu-id="a96a3-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="a96a3-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a96a3-116">Examples</span></span>

<span data-ttu-id="a96a3-117">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="a96a3-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="a96a3-118">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a96a3-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a96a3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a96a3-119">Requirements</span></span>



| <span data-ttu-id="a96a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a96a3-120">Requirement</span></span> | <span data-ttu-id="a96a3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a96a3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a96a3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a96a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a96a3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a96a3-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a96a3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a96a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a96a3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a96a3-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a96a3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a96a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96a3-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a96a3-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a96a3-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a96a3-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a96a3-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a96a3-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a96a3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a96a3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a96a3-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a96a3-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a96a3-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="a96a3-132">CLSID</span></span><br/>                    | <span data-ttu-id="a96a3-133">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="a96a3-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a96a3-134">IID</span><span class="sxs-lookup"><span data-stu-id="a96a3-134">IID</span></span><br/>                      | <span data-ttu-id="a96a3-135">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="a96a3-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a96a3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a96a3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96a3-137">**SWbemDateTime. MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="a96a3-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="a96a3-138">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a96a3-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="a96a3-139">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="a96a3-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

