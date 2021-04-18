---
description: Obtém ou define a representação UTC (tempo Universal Coordenado) do valor DateTime.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. UTC (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810864"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="a628d-103">Propriedade SWbemDateTime. UTC</span><span class="sxs-lookup"><span data-stu-id="a628d-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="a628d-104">A propriedade **UTC** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define a representação UTC (tempo Universal Coordenado) do valor **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a628d-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="a628d-105">O UTC é o tempo definido pelo padrão de tempo mundial.</span><span class="sxs-lookup"><span data-stu-id="a628d-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="a628d-106">O UTC substituiu o horário de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="a628d-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="a628d-107">Um valor UTC com um deslocamento zero é o mesmo que GMT com um deslocamento zero.</span><span class="sxs-lookup"><span data-stu-id="a628d-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="a628d-108">O número assinado deve estar no intervalo de-720 até 720 ou o erro **wbemErrValueOutOfRange** é retornado.</span><span class="sxs-lookup"><span data-stu-id="a628d-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="a628d-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a628d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a628d-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a628d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a628d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a628d-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="a628d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a628d-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="a628d-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a628d-113">Error codes</span></span>

<span data-ttu-id="a628d-114">Depois de obter ou definir a propriedade **UTC** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="a628d-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="a628d-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="a628d-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="a628d-116">O valor não estava no intervalo de-720 até 720.</span><span class="sxs-lookup"><span data-stu-id="a628d-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a628d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a628d-117">Examples</span></span>

<span data-ttu-id="a628d-118">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="a628d-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="a628d-119">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a628d-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a628d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a628d-120">Requirements</span></span>



| <span data-ttu-id="a628d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a628d-121">Requirement</span></span> | <span data-ttu-id="a628d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a628d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a628d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a628d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a628d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a628d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a628d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a628d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a628d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a628d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a628d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a628d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a628d-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a628d-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a628d-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a628d-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="a628d-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a628d-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a628d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a628d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a628d-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a628d-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a628d-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="a628d-133">CLSID</span></span><br/>                    | <span data-ttu-id="a628d-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="a628d-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a628d-135">IID</span><span class="sxs-lookup"><span data-stu-id="a628d-135">IID</span></span><br/>                      | <span data-ttu-id="a628d-136">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="a628d-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a628d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a628d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a628d-138">**SWbemDateTime. UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="a628d-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="a628d-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a628d-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="a628d-140">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="a628d-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

