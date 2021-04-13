---
description: A \_ estrutura informações do trabalho \_ 1 especifica as informações do trabalho de impressão, como o valor do identificador de trabalho, o nome da impressora para a qual o trabalho está em spool, o nome do computador que criou o trabalho de impressão, o nome do usuário que possui o trabalho de impressão e assim por diante.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Estrutura de JOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297465"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="91ba2-103">Estrutura de informações do trabalho \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="91ba2-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="91ba2-104">A **estrutura \_ informações \_ do trabalho 1** especifica as informações do trabalho de impressão, como o valor do identificador de trabalho, o nome da impressora para a qual o trabalho está em spool, o nome do computador que criou o trabalho de impressão, o nome do usuário que possui o trabalho de impressão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="91ba2-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ba2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91ba2-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="91ba2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="91ba2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="91ba2-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="91ba2-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-108">Um identificador de trabalho.</span><span class="sxs-lookup"><span data-stu-id="91ba2-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="91ba2-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora para a qual o trabalho está no spool.</span><span class="sxs-lookup"><span data-stu-id="91ba2-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="91ba2-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do computador que criou o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="91ba2-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que possui o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="91ba2-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do trabalho de impressão (por exemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="91ba2-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-117">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="91ba2-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-118">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-119">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="91ba2-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-120">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="91ba2-121">Esse membro deve ser verificado antes do *status* e, se *pStatus* for **nulo**, o status será definido pelo conteúdo do membro de status.</span><span class="sxs-lookup"><span data-stu-id="91ba2-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-122">**Status**</span><span class="sxs-lookup"><span data-stu-id="91ba2-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-123">O status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="91ba2-123">The job status.</span></span> <span data-ttu-id="91ba2-124">O valor desse membro pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="91ba2-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="91ba2-125">Um valor de zero indica que a fila de impressão foi pausada após o término do spool do documento.</span><span class="sxs-lookup"><span data-stu-id="91ba2-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="91ba2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="91ba2-126">Value</span></span>                           | <span data-ttu-id="91ba2-127">Significado</span><span class="sxs-lookup"><span data-stu-id="91ba2-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ba2-128">STATUS do trabalho \_ \_ bloqueado \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="91ba2-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="91ba2-129">O driver não pode imprimir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="91ba2-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="91ba2-130">STATUS do trabalho \_ \_ concluído</span><span class="sxs-lookup"><span data-stu-id="91ba2-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="91ba2-131">**Windows XP e posterior:** O trabalho é enviado para a impressora, mas o trabalho pode não ser impresso ainda.</span><span class="sxs-lookup"><span data-stu-id="91ba2-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="91ba2-132">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="91ba2-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="91ba2-133">STATUS do trabalho \_ \_ excluído</span><span class="sxs-lookup"><span data-stu-id="91ba2-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="91ba2-134">O trabalho foi excluído.</span><span class="sxs-lookup"><span data-stu-id="91ba2-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="91ba2-135">\_exclusão do status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="91ba2-136">O trabalho está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="91ba2-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="91ba2-137">\_erro de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="91ba2-138">Um erro está associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="91ba2-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="91ba2-139">STATUS do trabalho \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="91ba2-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="91ba2-140">A impressora está offline.</span><span class="sxs-lookup"><span data-stu-id="91ba2-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="91ba2-141">\_papel de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="91ba2-142">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="91ba2-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="91ba2-143">STATUS do trabalho em \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="91ba2-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="91ba2-144">O trabalho está em pausa.</span><span class="sxs-lookup"><span data-stu-id="91ba2-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="91ba2-145">STATUS do trabalho \_ \_ impresso</span><span class="sxs-lookup"><span data-stu-id="91ba2-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="91ba2-146">O trabalho foi impresso.</span><span class="sxs-lookup"><span data-stu-id="91ba2-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="91ba2-147">\_impressão do status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="91ba2-148">O trabalho está sendo impresso.</span><span class="sxs-lookup"><span data-stu-id="91ba2-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="91ba2-149">reinicialização do status do trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="91ba2-150">O trabalho foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="91ba2-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="91ba2-151">STATUS do trabalho \_ \_ retido</span><span class="sxs-lookup"><span data-stu-id="91ba2-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="91ba2-152">**Windows Vista e posterior:** O trabalho foi retido na fila de impressão e não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="91ba2-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="91ba2-153">Isso pode ser provocado pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="91ba2-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="91ba2-154">1) o trabalho foi retido manualmente por uma chamada para SetJob e o spooler está aguardando o trabalho ser liberado.</span><span class="sxs-lookup"><span data-stu-id="91ba2-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="91ba2-155">2) o trabalho não concluiu a impressão e deve concluir a impressão antes de poder ser excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91ba2-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="91ba2-156">Consulte [**SetJob**](setjob.md) para obter mais informações sobre os comandos de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="91ba2-157">\_spool de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="91ba2-158">O trabalho está em spool.</span><span class="sxs-lookup"><span data-stu-id="91ba2-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="91ba2-159">\_ \_ \_ intervenção do usuário do status do trabalho</span><span class="sxs-lookup"><span data-stu-id="91ba2-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="91ba2-160">A impressora tem um erro que exige que o usuário faça algo.</span><span class="sxs-lookup"><span data-stu-id="91ba2-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="91ba2-161">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="91ba2-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-162">A prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="91ba2-162">The job priority.</span></span> <span data-ttu-id="91ba2-163">Esse membro pode ser um dos valores a seguir ou no intervalo entre 1 e 99 (prioridade mínima \_ até a \_ prioridade máxima).</span><span class="sxs-lookup"><span data-stu-id="91ba2-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="91ba2-164">Valor</span><span class="sxs-lookup"><span data-stu-id="91ba2-164">Value</span></span>         | <span data-ttu-id="91ba2-165">Significado</span><span class="sxs-lookup"><span data-stu-id="91ba2-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="91ba2-166">\_prioridade mínima</span><span class="sxs-lookup"><span data-stu-id="91ba2-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="91ba2-167">Prioridade mínima.</span><span class="sxs-lookup"><span data-stu-id="91ba2-167">Minimum priority.</span></span> |
| <span data-ttu-id="91ba2-168">\_prioridade máxima</span><span class="sxs-lookup"><span data-stu-id="91ba2-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="91ba2-169">Prioridade máxima.</span><span class="sxs-lookup"><span data-stu-id="91ba2-169">Maximum priority.</span></span> |
| <span data-ttu-id="91ba2-170">prioridade de DEF. \_</span><span class="sxs-lookup"><span data-stu-id="91ba2-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="91ba2-171">Prioridade padrão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="91ba2-172">**Posição**</span><span class="sxs-lookup"><span data-stu-id="91ba2-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-173">A posição do trabalho na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="91ba2-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-175">O número total de páginas que o documento contém.</span><span class="sxs-lookup"><span data-stu-id="91ba2-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="91ba2-176">Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.</span><span class="sxs-lookup"><span data-stu-id="91ba2-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-177">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="91ba2-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-178">O número de páginas que foram impressas.</span><span class="sxs-lookup"><span data-stu-id="91ba2-178">The number of pages that have printed.</span></span> <span data-ttu-id="91ba2-179">Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.</span><span class="sxs-lookup"><span data-stu-id="91ba2-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="91ba2-180">**Enviado**</span><span class="sxs-lookup"><span data-stu-id="91ba2-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="91ba2-181">Uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que este documento foi colocado em spool.</span><span class="sxs-lookup"><span data-stu-id="91ba2-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="91ba2-182">Esse valor de tempo está no formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="91ba2-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="91ba2-183">Você deve convertê-lo em um valor de hora local antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="91ba2-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="91ba2-184">Você pode usar a função [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="91ba2-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91ba2-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="91ba2-185">Remarks</span></span>

<span data-ttu-id="91ba2-186">Os monitores de porta que não dão suporte a TrueEndOfJob definirão o trabalho como status de trabalho \_ \_ impresso logo depois que o trabalho for enviado para a impressora.</span><span class="sxs-lookup"><span data-stu-id="91ba2-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ba2-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ba2-187">Requirements</span></span>



| <span data-ttu-id="91ba2-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ba2-188">Requirement</span></span> | <span data-ttu-id="91ba2-189">Valor</span><span class="sxs-lookup"><span data-stu-id="91ba2-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ba2-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ba2-190">Minimum supported client</span></span><br/> | <span data-ttu-id="91ba2-191">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="91ba2-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="91ba2-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ba2-192">Minimum supported server</span></span><br/> | <span data-ttu-id="91ba2-193">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="91ba2-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="91ba2-194">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="91ba2-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ba2-195"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91ba2-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="91ba2-196">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="91ba2-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="91ba2-197">**\_ Informações do trabalho \_ \_ 1W** (Unicode) e **\_ info do trabalho \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="91ba2-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="91ba2-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="91ba2-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ba2-199">Impressão</span><span class="sxs-lookup"><span data-stu-id="91ba2-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="91ba2-200">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="91ba2-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="91ba2-201">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="91ba2-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="91ba2-202">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="91ba2-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="91ba2-203">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="91ba2-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

