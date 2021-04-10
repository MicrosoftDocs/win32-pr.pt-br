---
description: A \_ estrutura informações do trabalho \_ 2 descreve um conjunto completo de valores associados a um trabalho.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: Estrutura de JOB_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171707"
---
# <a name="job_info_2-structure"></a><span data-ttu-id="1ece0-103">Estrutura de informações do trabalho \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="1ece0-103">JOB\_INFO\_2 structure</span></span>

<span data-ttu-id="1ece0-104">A **estrutura \_ informações \_ do trabalho 2** descreve um conjunto completo de valores associados a um trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-104">The **JOB\_INFO\_2** structure describes a full set of values associated with a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ece0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ece0-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a><span data-ttu-id="1ece0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1ece0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ece0-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="1ece0-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-108">Um valor de identificador de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="1ece0-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora para a qual o trabalho está no spool.</span><span class="sxs-lookup"><span data-stu-id="1ece0-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="1ece0-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do computador que criou o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="1ece0-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que possui o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="1ece0-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do trabalho de impressão (por exemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="1ece0-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="1ece0-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-118">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que deve ser notificado quando o trabalho foi impresso ou quando ocorre um erro durante a impressão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="1ece0-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-120">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="1ece0-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-122">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão que deve ser usado para imprimir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="1ece0-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-124">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros do processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="1ece0-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-126">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora que deve ser usado para processar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="1ece0-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-128">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém dados de inicialização de dispositivo e de ambiente para o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1ece0-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="1ece0-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-130">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="1ece0-131">Esse membro deve ser verificado antes do **status** e, se **pStatus** for **nulo**, o status será definido pelo conteúdo do membro de status.</span><span class="sxs-lookup"><span data-stu-id="1ece0-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1ece0-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-133">O valor deste membro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1ece0-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="1ece0-134">Não há suporte para recuperação e configuração de descritores de segurança de documento nesta versão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="1ece0-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-136">O status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-136">The job status.</span></span> <span data-ttu-id="1ece0-137">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ece0-137">This member can be one or more of the following values.</span></span>

| <span data-ttu-id="1ece0-138">Valor</span><span class="sxs-lookup"><span data-stu-id="1ece0-138">Value</span></span>                           | <span data-ttu-id="1ece0-139">Significado</span><span class="sxs-lookup"><span data-stu-id="1ece0-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1ece0-140">STATUS do trabalho \_ \_ bloqueado \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="1ece0-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="1ece0-141">O driver não pode imprimir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="1ece0-142">STATUS do trabalho \_ \_ excluído</span><span class="sxs-lookup"><span data-stu-id="1ece0-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="1ece0-143">O trabalho foi excluído.</span><span class="sxs-lookup"><span data-stu-id="1ece0-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="1ece0-144">\_exclusão do status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="1ece0-145">O trabalho está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="1ece0-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="1ece0-146">\_erro de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="1ece0-147">Um erro está associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="1ece0-148">STATUS do trabalho \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="1ece0-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="1ece0-149">A impressora está offline.</span><span class="sxs-lookup"><span data-stu-id="1ece0-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="1ece0-150">\_papel de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="1ece0-151">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="1ece0-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="1ece0-152">STATUS do trabalho em \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="1ece0-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="1ece0-153">O trabalho está em pausa.</span><span class="sxs-lookup"><span data-stu-id="1ece0-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="1ece0-154">STATUS do trabalho \_ \_ impresso</span><span class="sxs-lookup"><span data-stu-id="1ece0-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="1ece0-155">O trabalho foi impresso.</span><span class="sxs-lookup"><span data-stu-id="1ece0-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="1ece0-156">\_impressão do status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="1ece0-157">O trabalho está sendo impresso.</span><span class="sxs-lookup"><span data-stu-id="1ece0-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="1ece0-158">reinicialização do status do trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="1ece0-159">O trabalho foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="1ece0-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="1ece0-160">\_spool de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="1ece0-161">O trabalho está em spool.</span><span class="sxs-lookup"><span data-stu-id="1ece0-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="1ece0-162">\_ \_ \_ intervenção do usuário do status do trabalho</span><span class="sxs-lookup"><span data-stu-id="1ece0-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="1ece0-163">A impressora tem um erro que exige que o usuário faça algo.</span><span class="sxs-lookup"><span data-stu-id="1ece0-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="1ece0-164">No Windows XP e versões posteriores do Windows, os seguintes valores também podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="1ece0-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="1ece0-165">Valor</span><span class="sxs-lookup"><span data-stu-id="1ece0-165">Value</span></span>                 | <span data-ttu-id="1ece0-166">Significado</span><span class="sxs-lookup"><span data-stu-id="1ece0-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ece0-167">STATUS do trabalho \_ \_ concluído</span><span class="sxs-lookup"><span data-stu-id="1ece0-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="1ece0-168">O trabalho é enviado para a impressora, mas pode não ser impresso ainda.</span><span class="sxs-lookup"><span data-stu-id="1ece0-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="1ece0-169">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1ece0-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="1ece0-170">STATUS do trabalho \_ \_ retido</span><span class="sxs-lookup"><span data-stu-id="1ece0-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="1ece0-171">O trabalho foi retido na fila de impressão após a impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="1ece0-172">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="1ece0-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-173">A prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-173">The job priority.</span></span> <span data-ttu-id="1ece0-174">Esse membro pode ser um dos valores a seguir ou no intervalo entre 1 e 99 (prioridade mínima \_ até a \_ prioridade máxima).</span><span class="sxs-lookup"><span data-stu-id="1ece0-174">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="1ece0-175">Valor</span><span class="sxs-lookup"><span data-stu-id="1ece0-175">Value</span></span>         | <span data-ttu-id="1ece0-176">Significado</span><span class="sxs-lookup"><span data-stu-id="1ece0-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="1ece0-177">\_prioridade mínima</span><span class="sxs-lookup"><span data-stu-id="1ece0-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="1ece0-178">Prioridade mínima.</span><span class="sxs-lookup"><span data-stu-id="1ece0-178">Minimum priority.</span></span> |
| <span data-ttu-id="1ece0-179">\_prioridade máxima</span><span class="sxs-lookup"><span data-stu-id="1ece0-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="1ece0-180">Prioridade máxima.</span><span class="sxs-lookup"><span data-stu-id="1ece0-180">Maximum priority.</span></span> |
| <span data-ttu-id="1ece0-181">prioridade de DEF. \_</span><span class="sxs-lookup"><span data-stu-id="1ece0-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="1ece0-182">Prioridade padrão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1ece0-183">**Posição**</span><span class="sxs-lookup"><span data-stu-id="1ece0-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-184">A posição do trabalho na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="1ece0-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-186">A hora mais antiga em que o trabalho pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="1ece0-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="1ece0-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-188">A hora mais recente em que o trabalho pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="1ece0-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="1ece0-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-190">O número de páginas necessárias para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-190">The number of pages required for the job.</span></span> <span data-ttu-id="1ece0-191">Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.</span><span class="sxs-lookup"><span data-stu-id="1ece0-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-192">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="1ece0-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-193">O tamanho, em bytes, do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ece0-193">The size, in bytes, of the job.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-194">**Enviado**</span><span class="sxs-lookup"><span data-stu-id="1ece0-194">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-195">Uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="1ece0-195">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="1ece0-196">Esse valor de tempo está no formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="1ece0-196">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="1ece0-197">Você deve convertê-lo em um valor de hora local antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="1ece0-197">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="1ece0-198">Você pode usar a função [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="1ece0-198">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-199">**Hora**</span><span class="sxs-lookup"><span data-stu-id="1ece0-199">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-200">O tempo total, em milissegundos, decorrido desde que o trabalho começou a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="1ece0-200">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="1ece0-201">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="1ece0-201">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="1ece0-202">O número de páginas que foram impressas.</span><span class="sxs-lookup"><span data-stu-id="1ece0-202">The number of pages that have printed.</span></span> <span data-ttu-id="1ece0-203">Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.</span><span class="sxs-lookup"><span data-stu-id="1ece0-203">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ece0-204">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ece0-204">Remarks</span></span>

<span data-ttu-id="1ece0-205">Os monitores de porta que não dão suporte a TrueEndOfJob definirão o trabalho como status de trabalho \_ \_ impresso logo depois que o trabalho for enviado para a impressora.</span><span class="sxs-lookup"><span data-stu-id="1ece0-205">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ece0-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ece0-206">Requirements</span></span>



| <span data-ttu-id="1ece0-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ece0-207">Requirement</span></span> | <span data-ttu-id="1ece0-208">Valor</span><span class="sxs-lookup"><span data-stu-id="1ece0-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ece0-209">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ece0-209">Minimum supported client</span></span><br/> | <span data-ttu-id="1ece0-210">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ece0-210">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1ece0-211">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ece0-211">Minimum supported server</span></span><br/> | <span data-ttu-id="1ece0-212">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ece0-212">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1ece0-213">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ece0-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ece0-214"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ece0-214"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1ece0-215">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1ece0-215">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ece0-216">**\_ Informações do trabalho \_ \_ 2W** (Unicode) e **\_ info do trabalho \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ece0-216">**\_JOB\_INFO\_2W** (Unicode) and **\_JOB\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="1ece0-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ece0-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ece0-218">Impressão</span><span class="sxs-lookup"><span data-stu-id="1ece0-218">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1ece0-219">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1ece0-219">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1ece0-220">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="1ece0-220">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="1ece0-221">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="1ece0-221">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="1ece0-222">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="1ece0-222">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="1ece0-223">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="1ece0-223">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

