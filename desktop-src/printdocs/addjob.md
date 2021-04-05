---
description: A função AddJob adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão. A função recupera o nome do arquivo que você pode usar para armazenar o trabalho.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Função AddJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662125"
---
# <a name="addjob-function"></a><span data-ttu-id="86050-104">Função AddJob</span><span class="sxs-lookup"><span data-stu-id="86050-104">AddJob function</span></span>

<span data-ttu-id="86050-105">A função **AddJob** adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="86050-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="86050-106">A função recupera o nome do arquivo que você pode usar para armazenar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="86050-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="86050-107">No Windows 8 e sistemas operacionais posteriores, não recomendamos o uso do **AddJob** diretamente porque há casos (como imprimir em uma fila usando o arquivo: ou PORTPROMPT:) em que **AddJob** falhará.</span><span class="sxs-lookup"><span data-stu-id="86050-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="86050-108">Em vez disso, é aconselhável usar a [API de impressão GDI](gdi-printing.md), a [API de impressão XPS](xps-printing.md), o [**StartDocPrinter**](startdocprinter.md)ou o método apropriado do namespace [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , dependendo do cenário de impressão.</span><span class="sxs-lookup"><span data-stu-id="86050-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="86050-109">Se você tentar imprimir em uma fila usando o **arquivo:** ou **PORTPROMPT:**, **AddJob** retornará o erro sem \_ suporte.</span><span class="sxs-lookup"><span data-stu-id="86050-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="86050-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86050-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="86050-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86050-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86050-112">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86050-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86050-113">Um identificador que especifica a impressora para o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="86050-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="86050-114">Essa deve ser uma impressora local configurada como uma impressora em spool.</span><span class="sxs-lookup"><span data-stu-id="86050-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="86050-115">Se *hPrinter* for um identificador para uma conexão de impressora remota, ou se a impressora estiver configurada para impressão direta, a função **AddJob** falhará.</span><span class="sxs-lookup"><span data-stu-id="86050-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="86050-116">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="86050-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="86050-117">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="86050-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86050-118">A versão da estrutura de dados de informações do trabalho de impressão que a função armazena no buffer apontado por *pData*.</span><span class="sxs-lookup"><span data-stu-id="86050-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="86050-119">Defina esse parâmetro como um.</span><span class="sxs-lookup"><span data-stu-id="86050-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="86050-120">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86050-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86050-121">Um ponteiro para um buffer que recebe uma estrutura de dados [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e uma cadeia de caracteres de caminho.</span><span class="sxs-lookup"><span data-stu-id="86050-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="86050-122">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86050-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86050-123">O tamanho, em bytes, do buffer apontado por *pData*.</span><span class="sxs-lookup"><span data-stu-id="86050-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="86050-124">O buffer precisa ser grande o suficiente para conter uma estrutura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e uma cadeia de caracteres de caminho.</span><span class="sxs-lookup"><span data-stu-id="86050-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="86050-125">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86050-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86050-126">Um ponteiro para uma variável que recebe o tamanho total, em bytes, da estrutura de dados [**ADDJOB \_ info \_ 1**](addjob-info-1.md) mais a cadeia de caracteres de caminho.</span><span class="sxs-lookup"><span data-stu-id="86050-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="86050-127">Se esse valor for menor ou igual a *cbBuf* e a função tiver sucesso, esse será o número real de bytes gravados no buffer apontado por *pData*.</span><span class="sxs-lookup"><span data-stu-id="86050-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="86050-128">Se esse número for maior que *cbBuf*, o buffer será muito pequeno e você deverá chamar a função novamente com um tamanho de buffer pelo menos tão grande quanto \* *pcbNeeded*.</span><span class="sxs-lookup"><span data-stu-id="86050-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86050-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86050-129">Return value</span></span>

<span data-ttu-id="86050-130">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="86050-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="86050-131">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="86050-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="86050-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="86050-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86050-133">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="86050-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="86050-134">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="86050-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="86050-135">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="86050-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="86050-136">Você pode chamar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o arquivo de spool especificado pelo membro **Path** da estrutura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e, em seguida, chamar a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para gravar dados de trabalho de impressão nele.</span><span class="sxs-lookup"><span data-stu-id="86050-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="86050-137">Depois disso, chame a função [**ScheduleJob**](schedulejob.md) para notificar o spooler de impressão de que o trabalho de impressão agora pode ser agendado pelo spooler para impressão.</span><span class="sxs-lookup"><span data-stu-id="86050-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="86050-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86050-138">Requirements</span></span>



| <span data-ttu-id="86050-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="86050-139">Requirement</span></span> | <span data-ttu-id="86050-140">Valor</span><span class="sxs-lookup"><span data-stu-id="86050-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86050-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86050-141">Minimum supported client</span></span><br/> | <span data-ttu-id="86050-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="86050-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86050-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86050-143">Minimum supported server</span></span><br/> | <span data-ttu-id="86050-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="86050-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="86050-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="86050-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="86050-146"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86050-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="86050-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86050-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="86050-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86050-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="86050-149">DLL</span><span class="sxs-lookup"><span data-stu-id="86050-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86050-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="86050-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="86050-151">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="86050-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="86050-152">**AddJobW** (Unicode) e **AddJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="86050-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="86050-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="86050-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86050-154">**Informações de ADDJOB \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="86050-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="86050-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="86050-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="86050-156">API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="86050-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="86050-157">Impressão</span><span class="sxs-lookup"><span data-stu-id="86050-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="86050-158">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="86050-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="86050-159">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="86050-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="86050-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="86050-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="86050-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="86050-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="86050-162">**Windows. Graphics. Printing**</span><span class="sxs-lookup"><span data-stu-id="86050-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="86050-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="86050-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="86050-164">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="86050-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

