---
description: Obtém ou define um valor que representa o componente de ano do valor DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Year (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789277"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="bffe2-103">Propriedade SWbemDateTime. Year</span><span class="sxs-lookup"><span data-stu-id="bffe2-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="bffe2-104">A propriedade **year** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de ano do valor [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="bffe2-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="bffe2-105">O valor deve estar no intervalo de 0000-9999 ou o erro wbemErrValueOutOfRange é retornado.</span><span class="sxs-lookup"><span data-stu-id="bffe2-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="bffe2-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bffe2-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bffe2-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bffe2-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffe2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bffe2-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="bffe2-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bffe2-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="bffe2-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bffe2-110">Error codes</span></span>

<span data-ttu-id="bffe2-111">Depois de obter ou definir a propriedade **year** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="bffe2-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="bffe2-112">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="bffe2-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="bffe2-113">O valor não estava no intervalo de 0000 a 9999.</span><span class="sxs-lookup"><span data-stu-id="bffe2-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bffe2-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bffe2-114">Examples</span></span>

<span data-ttu-id="bffe2-115">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="bffe2-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="bffe2-116">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="bffe2-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bffe2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bffe2-117">Requirements</span></span>



| <span data-ttu-id="bffe2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bffe2-118">Requirement</span></span> | <span data-ttu-id="bffe2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bffe2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bffe2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bffe2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bffe2-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bffe2-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bffe2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bffe2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bffe2-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bffe2-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bffe2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bffe2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bffe2-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bffe2-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bffe2-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bffe2-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="bffe2-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bffe2-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bffe2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bffe2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bffe2-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bffe2-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bffe2-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="bffe2-130">CLSID</span></span><br/>                    | <span data-ttu-id="bffe2-131">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="bffe2-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="bffe2-132">IID</span><span class="sxs-lookup"><span data-stu-id="bffe2-132">IID</span></span><br/>                      | <span data-ttu-id="bffe2-133">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="bffe2-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bffe2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="bffe2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffe2-135">**SWbemDateTime. YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="bffe2-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="bffe2-136">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="bffe2-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="bffe2-137">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="bffe2-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

