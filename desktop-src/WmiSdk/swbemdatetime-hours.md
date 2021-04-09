---
description: Obtém ou define um valor que representa o componente de horas do valor DateTime.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. hours (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171439"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="23b4b-103">Propriedade SWbemDateTime. hours</span><span class="sxs-lookup"><span data-stu-id="23b4b-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="23b4b-104">A propriedade **hours** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de horas do valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="23b4b-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="23b4b-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="23b4b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="23b4b-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="23b4b-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b4b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23b4b-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="23b4b-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="23b4b-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="23b4b-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="23b4b-109">Error codes</span></span>

<span data-ttu-id="23b4b-110">Depois de obter ou definir a propriedade **hours** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="23b4b-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="23b4b-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="23b4b-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="23b4b-112">O valor não estava no intervalo de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="23b4b-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="23b4b-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23b4b-113">Examples</span></span>

<span data-ttu-id="23b4b-114">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="23b4b-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="23b4b-115">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="23b4b-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23b4b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b4b-116">Requirements</span></span>



| <span data-ttu-id="23b4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b4b-117">Requirement</span></span> | <span data-ttu-id="23b4b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="23b4b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23b4b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23b4b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23b4b-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23b4b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23b4b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23b4b-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23b4b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23b4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b4b-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23b4b-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="23b4b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="23b4b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="23b4b-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23b4b-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23b4b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="23b4b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b4b-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b4b-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="23b4b-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="23b4b-129">CLSID</span></span><br/>                    | <span data-ttu-id="23b4b-130">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="23b4b-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="23b4b-131">IID</span><span class="sxs-lookup"><span data-stu-id="23b4b-131">IID</span></span><br/>                      | <span data-ttu-id="23b4b-132">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="23b4b-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="23b4b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="23b4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b4b-134">**SWbemDateTime. HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="23b4b-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="23b4b-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="23b4b-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="23b4b-136">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="23b4b-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

