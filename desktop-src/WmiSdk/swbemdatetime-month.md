---
description: Obtém ou define um valor que representa o componente de mês do valor DateTime.
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Month (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807295"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="526e1-103">Propriedade SWbemDateTime. Month</span><span class="sxs-lookup"><span data-stu-id="526e1-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="526e1-104">A propriedade **month** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de mês do valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="526e1-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="526e1-105">O número deve estar no intervalo de 01 a 12 ou o erro **wbemValueOutOfRange** é retornado.</span><span class="sxs-lookup"><span data-stu-id="526e1-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="526e1-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="526e1-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="526e1-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="526e1-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="526e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="526e1-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="526e1-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="526e1-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="526e1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="526e1-110">Examples</span></span>

<span data-ttu-id="526e1-111">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="526e1-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="526e1-112">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="526e1-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="526e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="526e1-113">Requirements</span></span>



| <span data-ttu-id="526e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="526e1-114">Requirement</span></span> | <span data-ttu-id="526e1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="526e1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="526e1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="526e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="526e1-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="526e1-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="526e1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="526e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="526e1-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="526e1-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="526e1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="526e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="526e1-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="526e1-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="526e1-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="526e1-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="526e1-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="526e1-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="526e1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="526e1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="526e1-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="526e1-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="526e1-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="526e1-126">CLSID</span></span><br/>                    | <span data-ttu-id="526e1-127">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="526e1-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="526e1-128">IID</span><span class="sxs-lookup"><span data-stu-id="526e1-128">IID</span></span><br/>                      | <span data-ttu-id="526e1-129">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="526e1-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="526e1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="526e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="526e1-131">**SWbemDateTime. MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="526e1-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="526e1-132">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="526e1-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="526e1-133">HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="526e1-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




