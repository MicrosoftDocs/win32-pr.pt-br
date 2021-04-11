---
description: Representa o contexto de execução quando GetPrintExecutionData é chamado.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Enumeração de PRINT_EXECUTION_CONTEXT (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169456"
---
# <a name="print_execution_context-enumeration"></a><span data-ttu-id="f1d83-103">Enumeração de contexto de \_ execução de impressão \_</span><span class="sxs-lookup"><span data-stu-id="f1d83-103">PRINT\_EXECUTION\_CONTEXT enumeration</span></span>

<span data-ttu-id="f1d83-104">Representa o contexto de execução quando [**GetPrintExecutionData**](getprintexecutiondata.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="f1d83-104">Represents the execution context when [**GetPrintExecutionData**](getprintexecutiondata.md) is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1d83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1d83-105">Syntax</span></span>


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="f1d83-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f1d83-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f1d83-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_aplicativo de \_ contexto de execução de impressão \_**</span><span class="sxs-lookup"><span data-stu-id="f1d83-107"><span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**PRINT\_EXECUTION\_CONTEXT\_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="f1d83-108">O chamador está sendo executado em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1d83-108">The caller is running in an application.</span></span>

</dd> <dt>

<span data-ttu-id="f1d83-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ serviço spooler do contexto de execução de \_ impressão \_**</span><span class="sxs-lookup"><span data-stu-id="f1d83-109"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="f1d83-110">O chamador está em execução no serviço de spooler (spoolsv.exe).</span><span class="sxs-lookup"><span data-stu-id="f1d83-110">The caller is running in the spooler service (spoolsv.exe).</span></span>

</dd> <dt>

<span data-ttu-id="f1d83-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_host de \_ isolamento do spooler do contexto de execução de \_ \_ impressão \_**</span><span class="sxs-lookup"><span data-stu-id="f1d83-111"><span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT\_EXECUTION\_CONTEXT\_SPOOLER\_ISOLATION\_HOST**</span></span>
</dt> <dd>

<span data-ttu-id="f1d83-112">O chamador está em execução no host de isolamento de impressão (PrintIsolationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="f1d83-112">The caller is running in the print isolation host (PrintIsolationHost.exe)</span></span>

</dd> <dt>

<span data-ttu-id="f1d83-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_pipeline de \_ filtro do contexto de execução de impressão \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f1d83-113"><span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PRINT\_EXECUTION\_CONTEXT\_FILTER\_PIPELINE**</span></span>
</dt> <dd>

<span data-ttu-id="f1d83-114">O chamador está em execução no pipeline de filtro de impressão (printfilterpipelinesvc.exe)</span><span class="sxs-lookup"><span data-stu-id="f1d83-114">The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)</span></span>

</dd> <dt>

<span data-ttu-id="f1d83-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Contexto de execução de impressão \_ \_ \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="f1d83-115"><span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT\_EXECUTION\_CONTEXT\_WOW64**</span></span>
</dt> <dd>

<span data-ttu-id="f1d83-116">O chamador está em execução no splwow64.exe</span><span class="sxs-lookup"><span data-stu-id="f1d83-116">The caller is running in splwow64.exe</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1d83-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1d83-117">Requirements</span></span>



| <span data-ttu-id="f1d83-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1d83-118">Requirement</span></span> | <span data-ttu-id="f1d83-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f1d83-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d83-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d83-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f1d83-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="f1d83-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d83-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f1d83-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f1d83-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1d83-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d83-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d83-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d83-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1d83-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d83-127">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="f1d83-127">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="f1d83-128">**IMPRIMIR \_ dados de execução \_**</span><span class="sxs-lookup"><span data-stu-id="f1d83-128">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

 




