---
description: Obtém ou define um valor que representa o componente de segundos do valor DateTime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Seconds (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793963"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="07a14-103">Propriedade SWbemDateTime. Seconds</span><span class="sxs-lookup"><span data-stu-id="07a14-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="07a14-104">A propriedade **Seconds** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define um valor que representa o componente de segundos do valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="07a14-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="07a14-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="07a14-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="07a14-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="07a14-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a14-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="07a14-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="07a14-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="07a14-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="07a14-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="07a14-109">Error codes</span></span>

<span data-ttu-id="07a14-110">Depois de obter ou definir a propriedade **Seconds** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="07a14-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="07a14-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="07a14-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="07a14-112">O valor não estava no intervalo de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="07a14-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07a14-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="07a14-113">Remarks</span></span>

<span data-ttu-id="07a14-114">A propriedade **SWbemDateTime. Seconds** pode conter um valor incorreto se a propriedade [**SWbemDateTime. Minutes**](swbemdatetime-minutes.md) tiver sido definida como 1.</span><span class="sxs-lookup"><span data-stu-id="07a14-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="07a14-115">Ele contém um valor que é deslocado em um segundo devido a um erro de arredondamento que ocorre quando um valor [**DateTime**](datetime.md) de CIM é convertido em um valor de **\_ Data VT** .</span><span class="sxs-lookup"><span data-stu-id="07a14-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="07a14-116">Se a propriedade **minutes** for definida como 0 (zero) em vez disso, a propriedade **segundos** retornará o valor correto.</span><span class="sxs-lookup"><span data-stu-id="07a14-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="07a14-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07a14-117">Examples</span></span>

<span data-ttu-id="07a14-118">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="07a14-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="07a14-119">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="07a14-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07a14-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07a14-120">Requirements</span></span>



| <span data-ttu-id="07a14-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a14-121">Requirement</span></span> | <span data-ttu-id="07a14-122">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a14-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07a14-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07a14-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07a14-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07a14-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07a14-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07a14-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a14-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07a14-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07a14-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a14-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a14-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="07a14-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="07a14-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="07a14-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="07a14-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="07a14-131">DLL</span><span class="sxs-lookup"><span data-stu-id="07a14-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a14-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a14-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="07a14-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="07a14-133">CLSID</span></span><br/>                    | <span data-ttu-id="07a14-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="07a14-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="07a14-135">IID</span><span class="sxs-lookup"><span data-stu-id="07a14-135">IID</span></span><br/>                      | <span data-ttu-id="07a14-136">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="07a14-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="07a14-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="07a14-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a14-138">**SWbemDateTime. SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="07a14-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="07a14-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="07a14-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="07a14-140">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="07a14-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

