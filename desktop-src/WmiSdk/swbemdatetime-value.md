---
description: Obtém ou define a data do CIM bruto no formato DMTF (Distributed Management Task Force).
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091292"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="97d57-103">Propriedade SWbemDateTime. Value</span><span class="sxs-lookup"><span data-stu-id="97d57-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="97d57-104">A propriedade **Value** do objeto [**SWbemDateTime**](swbemdatetime.md) Obtém ou define a data do CIM bruto no formato DMTF (Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="97d57-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="97d57-105">O formato DMTF é uma representação de cadeia de caracteres do valor [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="97d57-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="97d57-106">Essa propriedade é a propriedade padrão para objetos **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="97d57-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="97d57-107">A propriedade **Value** tem um valor padrão de 00000101000000.000000 + 000.</span><span class="sxs-lookup"><span data-stu-id="97d57-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="97d57-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="97d57-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="97d57-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="97d57-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d57-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="97d57-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="97d57-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="97d57-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="97d57-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="97d57-112">Error codes</span></span>

<span data-ttu-id="97d57-113">Depois de obter ou definir a propriedade **Value** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) poderá conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="97d57-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="97d57-114">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="97d57-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="97d57-115">O *formato de um* não é válido.</span><span class="sxs-lookup"><span data-stu-id="97d57-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="97d57-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97d57-116">Examples</span></span>

<span data-ttu-id="97d57-117">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="97d57-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="97d57-118">Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="97d57-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97d57-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97d57-119">Requirements</span></span>



| <span data-ttu-id="97d57-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="97d57-120">Requirement</span></span> | <span data-ttu-id="97d57-121">Valor</span><span class="sxs-lookup"><span data-stu-id="97d57-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d57-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97d57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="97d57-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97d57-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97d57-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97d57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="97d57-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97d57-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97d57-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97d57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d57-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d57-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97d57-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="97d57-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="97d57-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97d57-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97d57-130">DLL</span><span class="sxs-lookup"><span data-stu-id="97d57-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97d57-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d57-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="97d57-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="97d57-132">CLSID</span></span><br/>                    | <span data-ttu-id="97d57-133">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="97d57-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="97d57-134">IID</span><span class="sxs-lookup"><span data-stu-id="97d57-134">IID</span></span><br/>                      | <span data-ttu-id="97d57-135">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="97d57-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="97d57-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="97d57-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d57-137">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="97d57-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="97d57-138">**HORÁRIO**</span><span class="sxs-lookup"><span data-stu-id="97d57-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

