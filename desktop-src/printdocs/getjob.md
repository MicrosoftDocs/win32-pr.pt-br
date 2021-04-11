---
description: A função GetJob recupera informações sobre um trabalho de impressão especificado.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Função GetJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169461"
---
# <a name="getjob-function"></a><span data-ttu-id="0554d-103">Função GetJob</span><span class="sxs-lookup"><span data-stu-id="0554d-103">GetJob function</span></span>

<span data-ttu-id="0554d-104">A função **GetJob** recupera informações sobre um trabalho de impressão especificado.</span><span class="sxs-lookup"><span data-stu-id="0554d-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="0554d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0554d-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="0554d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0554d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0554d-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0554d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0554d-108">Um identificador para a impressora para a qual os dados de trabalho de impressão são recuperados.</span><span class="sxs-lookup"><span data-stu-id="0554d-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="0554d-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="0554d-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="0554d-110">*JobID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0554d-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0554d-111">Identifica o trabalho de impressão para o qual recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="0554d-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="0554d-112">Use a função [**AddJob**](addjob.md) ou a função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obter um identificador de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="0554d-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0554d-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0554d-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0554d-114">O tipo de informação retornado no buffer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="0554d-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="0554d-115">Se o *nível* for 1, *pJob* receberá uma estrutura de [**informações de trabalho \_ \_ 1**](job-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="0554d-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="0554d-116">Se *Level* for 2, *pJob* receberá uma estrutura de [**informações de trabalho \_ \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="0554d-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0554d-117">*pJob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0554d-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0554d-118">Um ponteiro para um buffer que recebe as informações de [**trabalho \_ \_ 1**](job-info-1.md) ou uma estrutura de [**informações de trabalho \_ \_ 2**](job-info-2.md) que contém informação sobre o trabalho.</span><span class="sxs-lookup"><span data-stu-id="0554d-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="0554d-119">O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="0554d-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="0554d-120">Para determinar o tamanho do buffer necessário, chame **GetJob** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="0554d-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="0554d-121">**GetJob** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="0554d-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="0554d-122">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0554d-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0554d-123">O tamanho, em bytes, da matriz.</span><span class="sxs-lookup"><span data-stu-id="0554d-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="0554d-124">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0554d-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0554d-125">Um ponteiro para um valor que especifica o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="0554d-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0554d-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0554d-126">Return value</span></span>

<span data-ttu-id="0554d-127">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0554d-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0554d-128">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="0554d-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0554d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="0554d-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0554d-130">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0554d-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0554d-131">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0554d-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0554d-132">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="0554d-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0554d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0554d-133">Requirements</span></span>



| <span data-ttu-id="0554d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0554d-134">Requirement</span></span> | <span data-ttu-id="0554d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0554d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0554d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0554d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0554d-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0554d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0554d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0554d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0554d-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0554d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0554d-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0554d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0554d-141"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0554d-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0554d-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0554d-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0554d-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0554d-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0554d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0554d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0554d-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0554d-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0554d-146">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0554d-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0554d-147">**GetJobW** (Unicode) e **GetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0554d-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="0554d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0554d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0554d-149">Impressão</span><span class="sxs-lookup"><span data-stu-id="0554d-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0554d-150">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="0554d-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0554d-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="0554d-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="0554d-152">**Informações do trabalho \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0554d-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="0554d-153">**Informações do trabalho \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0554d-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="0554d-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="0554d-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="0554d-155">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="0554d-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

