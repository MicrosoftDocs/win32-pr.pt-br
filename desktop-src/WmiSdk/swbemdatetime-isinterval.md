---
description: Valor booliano que indica se qualquer campo em um valor de data e hora CIM deve ser interpretado como um intervalo.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. isinterval (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171974"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="5fc2c-103">Propriedade SWbemDateTime. isinterval</span><span class="sxs-lookup"><span data-stu-id="5fc2c-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="5fc2c-104">A propriedade **isinterval** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se qualquer campo em um valor de data e hora CIM deve ser interpretado como um intervalo.</span><span class="sxs-lookup"><span data-stu-id="5fc2c-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="5fc2c-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5fc2c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5fc2c-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5fc2c-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc2c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fc2c-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="5fc2c-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5fc2c-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="5fc2c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5fc2c-109">Examples</span></span>

<span data-ttu-id="5fc2c-110">Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e hora CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="5fc2c-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="5fc2c-111">Para obter uma descrição do formato de [data e hora CIM, consulte formato de datas e horas](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="5fc2c-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc2c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc2c-112">Requirements</span></span>



| <span data-ttu-id="5fc2c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc2c-113">Requirement</span></span> | <span data-ttu-id="5fc2c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5fc2c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc2c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc2c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc2c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fc2c-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5fc2c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc2c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc2c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fc2c-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5fc2c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fc2c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc2c-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc2c-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5fc2c-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5fc2c-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5fc2c-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5fc2c-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5fc2c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5fc2c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fc2c-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fc2c-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5fc2c-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="5fc2c-125">CLSID</span></span><br/>                    | <span data-ttu-id="5fc2c-126">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="5fc2c-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="5fc2c-127">IID</span><span class="sxs-lookup"><span data-stu-id="5fc2c-127">IID</span></span><br/>                      | <span data-ttu-id="5fc2c-128">ISWbemDateTime de IID \_</span><span class="sxs-lookup"><span data-stu-id="5fc2c-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5fc2c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc2c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc2c-130">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5fc2c-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="5fc2c-131">Formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="5fc2c-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




