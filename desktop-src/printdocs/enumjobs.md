---
description: A função EnumJobs recupera informações sobre um conjunto especificado de trabalhos de impressão para uma impressora especificada.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Função EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170507"
---
# <a name="enumjobs-function"></a><span data-ttu-id="e75a1-103">Função EnumJobs</span><span class="sxs-lookup"><span data-stu-id="e75a1-103">EnumJobs function</span></span>

<span data-ttu-id="e75a1-104">A função **EnumJobs** recupera informações sobre um conjunto especificado de trabalhos de impressão para uma impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="e75a1-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e75a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e75a1-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="e75a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e75a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e75a1-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-108">Um identificador para o objeto de impressora cujos trabalhos de impressão a função enumera.</span><span class="sxs-lookup"><span data-stu-id="e75a1-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="e75a1-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="e75a1-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e75a1-110">*FirstJob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-111">A posição de base zero dentro da fila de impressão do primeiro trabalho de impressão a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="e75a1-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="e75a1-112">Por exemplo, um valor de 0 especifica que a enumeração deve começar no primeiro trabalho de impressão na fila de impressão; um valor de 9 especifica que a enumeração deve começar no décimo trabalho de impressão na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="e75a1-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="e75a1-113">*Nojobs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-114">O número total de trabalhos de impressão a serem enumerados.</span><span class="sxs-lookup"><span data-stu-id="e75a1-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="e75a1-115">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-116">O tipo de informação retornado no buffer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="e75a1-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="e75a1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e75a1-117">Value</span></span>                                                                                                | <span data-ttu-id="e75a1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e75a1-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="e75a1-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e75a1-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e75a1-120">*pJob* recebe uma matriz de estruturas de [**informações de trabalho \_ \_ 1**](job-info-1.md)</span><span class="sxs-lookup"><span data-stu-id="e75a1-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="e75a1-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e75a1-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e75a1-122">*pJob* recebe uma matriz de estruturas de [**informações de trabalho \_ \_ 2**](job-info-2.md)</span><span class="sxs-lookup"><span data-stu-id="e75a1-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="e75a1-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="e75a1-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e75a1-124">*pJob* recebe uma matriz de estruturas de [**informações de trabalho \_ \_ 3**](job-info-3.md)</span><span class="sxs-lookup"><span data-stu-id="e75a1-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e75a1-125">*pJob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-126">Um ponteiro para um buffer que recebe uma matriz das [**estruturas \_ informações \_ do trabalho 1**](job-info-1.md), informações do [**trabalho \_ \_ 2**](job-info-2.md)ou [**informações do trabalho \_ \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="e75a1-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="e75a1-127">O buffer deve ser grande o suficiente para receber a matriz de estruturas e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.</span><span class="sxs-lookup"><span data-stu-id="e75a1-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="e75a1-128">Para determinar o tamanho do buffer necessário, chame **EnumJobs** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="e75a1-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="e75a1-129">**EnumJobs** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="e75a1-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="e75a1-130">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-131">O tamanho, em bytes, do buffer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="e75a1-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e75a1-132">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-133">Um ponteiro para uma variável que recebe o número de bytes copiados se a função for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e75a1-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="e75a1-134">Se a função falhar, a variável receberá o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="e75a1-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="e75a1-135">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e75a1-136">Um ponteiro para uma variável que recebe o número de estruturas de informações do trabalho [**\_ \_ 1**](job-info-1.md), [**informações do trabalho \_ \_ 2**](job-info-2.md)ou [**informações do trabalho \_ \_ 3**](job-info-3.md) retornadas no buffer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="e75a1-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e75a1-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e75a1-137">Return value</span></span>

<span data-ttu-id="e75a1-138">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e75a1-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e75a1-139">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="e75a1-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e75a1-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="e75a1-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e75a1-141">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e75a1-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e75a1-142">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e75a1-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e75a1-143">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e75a1-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e75a1-144">A [**estrutura \_ informações \_ do trabalho 1**](job-info-1.md) contém informações gerais de trabalho de impressão; a estrutura [**informações do trabalho \_ \_ 2**](job-info-2.md) tem informações muito mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="e75a1-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="e75a1-145">A [**estrutura \_ informações \_ do trabalho 3**](job-info-3.md) contém informações sobre como os trabalhos são vinculados.</span><span class="sxs-lookup"><span data-stu-id="e75a1-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="e75a1-146">Para determinar o número de trabalhos de impressão na fila de impressora, chame a função [**Getprinter**](getprinter.md) com o parâmetro *Level* definido como 2.</span><span class="sxs-lookup"><span data-stu-id="e75a1-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75a1-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e75a1-147">Requirements</span></span>



| <span data-ttu-id="e75a1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e75a1-148">Requirement</span></span> | <span data-ttu-id="e75a1-149">Valor</span><span class="sxs-lookup"><span data-stu-id="e75a1-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75a1-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e75a1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e75a1-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e75a1-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e75a1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e75a1-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e75a1-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e75a1-154">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e75a1-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e75a1-155"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e75a1-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e75a1-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e75a1-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="e75a1-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e75a1-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e75a1-158">DLL</span><span class="sxs-lookup"><span data-stu-id="e75a1-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e75a1-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e75a1-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e75a1-160">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e75a1-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e75a1-161">**EnumJobsW** (Unicode) e **EnumJobsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e75a1-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="e75a1-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="e75a1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75a1-163">Impressão</span><span class="sxs-lookup"><span data-stu-id="e75a1-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e75a1-164">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e75a1-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e75a1-165">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="e75a1-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="e75a1-166">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="e75a1-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="e75a1-167">**Informações do trabalho \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e75a1-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="e75a1-168">**Informações do trabalho \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e75a1-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="e75a1-169">**Informações do trabalho \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e75a1-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="e75a1-170">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e75a1-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e75a1-171">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="e75a1-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

