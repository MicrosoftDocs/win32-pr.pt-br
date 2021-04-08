---
description: Relata para o serviço spooler de impressão se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização e qual parte do processamento está em andamento no momento.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Função ReportJobProcessingProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922170"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="e8c33-103">Função ReportJobProcessingProgress</span><span class="sxs-lookup"><span data-stu-id="e8c33-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="e8c33-104">Relata para o serviço spooler de impressão se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização e qual parte do processamento está em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="e8c33-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c33-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8c33-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="e8c33-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c33-107">*printerHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8c33-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c33-108">Um identificador de impressora para o qual a função deve recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="e8c33-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="e8c33-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="e8c33-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e8c33-110">*jobId* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e8c33-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c33-111">Identifica o trabalho de impressão para o qual recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="e8c33-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="e8c33-112">Use a função [**AddJob**](addjob.md) ou a função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obter um identificador de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="e8c33-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8c33-113">*jobOperation*</span><span class="sxs-lookup"><span data-stu-id="e8c33-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c33-114">Especifica se o trabalho está na fase de spool ou na fase de renderização.</span><span class="sxs-lookup"><span data-stu-id="e8c33-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="e8c33-115">*jobProgress*</span><span class="sxs-lookup"><span data-stu-id="e8c33-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c33-116">Especifica qual parte do processamento está atualmente em andamento.</span><span class="sxs-lookup"><span data-stu-id="e8c33-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="e8c33-117">Esse valor se refere a eventos na fase de processamento em spool ou de renderização, dependendo do valor de *jobOperation*.</span><span class="sxs-lookup"><span data-stu-id="e8c33-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c33-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8c33-118">Return value</span></span>

<span data-ttu-id="e8c33-119">Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e8c33-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="e8c33-120">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="e8c33-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c33-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8c33-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8c33-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e8c33-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e8c33-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8c33-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e8c33-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e8c33-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="e8c33-125">O **ReportJobProcessingProgress** só relatará o progresso do trabalho de impressão XPS se o trabalho de impressão estiver na fase de processamento em spool ou de renderização.</span><span class="sxs-lookup"><span data-stu-id="e8c33-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="e8c33-126">O **ReportJobProcessingProgress** falhará se for chamado quando o trabalho de impressão XPS não estiver na fase de processamento em spool ou de renderização.</span><span class="sxs-lookup"><span data-stu-id="e8c33-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8c33-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c33-127">Requirements</span></span>



| <span data-ttu-id="e8c33-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c33-128">Requirement</span></span> | <span data-ttu-id="e8c33-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e8c33-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c33-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8c33-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c33-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8c33-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e8c33-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8c33-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c33-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8c33-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8c33-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8c33-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8c33-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8c33-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e8c33-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8c33-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8c33-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8c33-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e8c33-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e8c33-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8c33-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c33-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e8c33-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8c33-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c33-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="e8c33-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e8c33-142">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e8c33-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e8c33-143">**EPrintXPSJobOperation**</span><span class="sxs-lookup"><span data-stu-id="e8c33-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="e8c33-144">**EPrintXPSJobProgress**</span><span class="sxs-lookup"><span data-stu-id="e8c33-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

