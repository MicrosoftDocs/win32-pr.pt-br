---
description: A \_ estrutura do \_ tipo de opções de notificação de impressora \_ especifica o conjunto de campos de informações de impressora ou trabalho a ser monitorado por um objeto de notificação de alteração de impressora. Uma chamada para a função FindFirstPrinterChangeNotification especifica uma \_ \_ estrutura de opções de notificação de impressora, que contém uma matriz de estruturas de tipo de opções de notificação de impressora \_ \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Estrutura de PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780312"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="66d2f-103">\_Estrutura do \_ tipo de opções de notificação de impressora \_</span><span class="sxs-lookup"><span data-stu-id="66d2f-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="66d2f-104">A estrutura do tipo de opções de notificação de impressora especifica o conjunto de campos de informações de impressora ou trabalho a ser monitorado por um objeto de notificação de alteração de impressora. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="66d2f-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="66d2f-105">Uma chamada para a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) especifica uma estrutura de [**\_ \_ Opções de notificação de impressora**](printer-notify-options.md) , que contém uma matriz de estruturas de **\_ \_ \_ tipo de opções de notificação de impressora** .</span><span class="sxs-lookup"><span data-stu-id="66d2f-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d2f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66d2f-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="66d2f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="66d2f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="66d2f-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66d2f-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="66d2f-109">O tipo a ser observado.</span><span class="sxs-lookup"><span data-stu-id="66d2f-109">The type to be watched.</span></span> <span data-ttu-id="66d2f-110">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="66d2f-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="66d2f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="66d2f-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="66d2f-112">Significado</span><span class="sxs-lookup"><span data-stu-id="66d2f-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="66d2f-113"><dt>**Trabalho \_ do NOTIFICAr \_ tipo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="66d2f-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="66d2f-114">Indica que os campos especificados na matriz **pFields** são constantes de \_ campo de notificação de trabalho \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="66d2f-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="66d2f-115"><dt>**Impressora \_ NOTIFICAr \_ tipo**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="66d2f-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="66d2f-116">Indica que os campos especificados na matriz **pFields** são constantes de \_ campo de notificação de impressora \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="66d2f-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="66d2f-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="66d2f-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="66d2f-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="66d2f-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="66d2f-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="66d2f-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="66d2f-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="66d2f-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="66d2f-121">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="66d2f-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="66d2f-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="66d2f-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="66d2f-123">**Count**</span><span class="sxs-lookup"><span data-stu-id="66d2f-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="66d2f-124">O número de elementos na matriz **pFields** .</span><span class="sxs-lookup"><span data-stu-id="66d2f-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="66d2f-125">**pFields**</span><span class="sxs-lookup"><span data-stu-id="66d2f-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="66d2f-126">Um ponteiro para uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="66d2f-126">A pointer to an array of values.</span></span> <span data-ttu-id="66d2f-127">Cada elemento da matriz Especifica um campo de informações de trabalho ou de impressora de interesse.</span><span class="sxs-lookup"><span data-stu-id="66d2f-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="66d2f-128">Para obter uma lista de campos de informações de impressora e de trabalho com suporte, consulte a estrutura de [**\_ \_ \_ dados informações de notificação de impressora**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="66d2f-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66d2f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d2f-129">Requirements</span></span>



| <span data-ttu-id="66d2f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d2f-130">Requirement</span></span> | <span data-ttu-id="66d2f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="66d2f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d2f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66d2f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="66d2f-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66d2f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66d2f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66d2f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="66d2f-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66d2f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="66d2f-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="66d2f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d2f-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66d2f-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d2f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="66d2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d2f-139">Impressão</span><span class="sxs-lookup"><span data-stu-id="66d2f-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="66d2f-140">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="66d2f-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="66d2f-141">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="66d2f-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="66d2f-142">**\_dados de \_ informações de notificação da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="66d2f-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="66d2f-143">**\_Opções de notificação de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="66d2f-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 




