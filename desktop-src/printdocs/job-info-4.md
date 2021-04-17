---
description: Descreve um conjunto completo de valores associados a um trabalho e dá suporte a arquivos de spool grandes com tamanhos expressos com 64 bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: Estrutura de JOB_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5a6ccd7bf589ed341c9aceab86205cd9852c0896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749485"
---
# <a name="job_info_4-structure"></a><span data-ttu-id="9f415-103">Estrutura das informações do trabalho \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="9f415-103">JOB\_INFO\_4 structure</span></span>

<span data-ttu-id="9f415-104">Descreve um conjunto completo de valores associados a um trabalho e dá suporte a arquivos de spool grandes com tamanhos expressos com 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9f415-104">Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f415-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f415-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_4 {
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
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a><span data-ttu-id="9f415-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9f415-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f415-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="9f415-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-108">Um valor de identificador de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="9f415-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora para a qual o trabalho está no spool.</span><span class="sxs-lookup"><span data-stu-id="9f415-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="9f415-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do computador que criou o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="9f415-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que possui o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="9f415-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do trabalho de impressão (por exemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="9f415-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="9f415-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="9f415-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-118">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que deve ser notificado quando o trabalho foi impresso ou quando ocorre um erro durante a impressão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed, or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="9f415-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-120">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="9f415-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-122">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão que deve ser usado para imprimir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="9f415-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-124">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros do processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="9f415-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-126">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora que deve ser usado para processar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="9f415-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-128">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém dados de inicialização de dispositivo e de ambiente para o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="9f415-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="9f415-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-130">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="9f415-131">Esse membro deve ser verificado antes do **status** e, se **pStatus** for **nulo**, o status será definido pelo conteúdo do membro de status.</span><span class="sxs-lookup"><span data-stu-id="9f415-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9f415-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-133">O valor deste membro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9f415-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="9f415-134">Não há suporte para recuperação e configuração de descritores de segurança de documento nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9f415-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="9f415-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-136">O status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-136">The job status.</span></span> <span data-ttu-id="9f415-137">Esse membro pode ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9f415-137">This member can be one or more of the following values:</span></span>

| <span data-ttu-id="9f415-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9f415-138">Value</span></span>                           | <span data-ttu-id="9f415-139">Significado</span><span class="sxs-lookup"><span data-stu-id="9f415-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9f415-140">STATUS do trabalho \_ \_ bloqueado \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="9f415-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="9f415-141">O driver não pode imprimir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="9f415-142">STATUS do trabalho \_ \_ excluído</span><span class="sxs-lookup"><span data-stu-id="9f415-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="9f415-143">O trabalho foi excluído.</span><span class="sxs-lookup"><span data-stu-id="9f415-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="9f415-144">\_exclusão do status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="9f415-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="9f415-145">O trabalho está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="9f415-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="9f415-146">\_erro de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="9f415-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="9f415-147">Um erro está associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="9f415-148">STATUS do trabalho \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="9f415-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="9f415-149">A impressora está offline.</span><span class="sxs-lookup"><span data-stu-id="9f415-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="9f415-150">\_papel de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="9f415-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="9f415-151">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="9f415-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="9f415-152">STATUS do trabalho em \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="9f415-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="9f415-153">O trabalho está em pausa.</span><span class="sxs-lookup"><span data-stu-id="9f415-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="9f415-154">STATUS do trabalho \_ \_ impresso</span><span class="sxs-lookup"><span data-stu-id="9f415-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="9f415-155">O trabalho foi impresso.</span><span class="sxs-lookup"><span data-stu-id="9f415-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="9f415-156">\_impressão do status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="9f415-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="9f415-157">O trabalho está sendo impresso.</span><span class="sxs-lookup"><span data-stu-id="9f415-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="9f415-158">reinicialização do status do trabalho \_ \_</span><span class="sxs-lookup"><span data-stu-id="9f415-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="9f415-159">O trabalho foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="9f415-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="9f415-160">\_spool de status do trabalho \_</span><span class="sxs-lookup"><span data-stu-id="9f415-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="9f415-161">O trabalho está em spool.</span><span class="sxs-lookup"><span data-stu-id="9f415-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="9f415-162">\_ \_ \_ intervenção do usuário do status do trabalho</span><span class="sxs-lookup"><span data-stu-id="9f415-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="9f415-163">A impressora tem um erro que exige que o usuário faça algo.</span><span class="sxs-lookup"><span data-stu-id="9f415-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="9f415-164">No Windows XP e versões posteriores do Windows, os seguintes valores também podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="9f415-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="9f415-165">Valor</span><span class="sxs-lookup"><span data-stu-id="9f415-165">Value</span></span>                 | <span data-ttu-id="9f415-166">Significado</span><span class="sxs-lookup"><span data-stu-id="9f415-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f415-167">STATUS do trabalho \_ \_ concluído</span><span class="sxs-lookup"><span data-stu-id="9f415-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="9f415-168">O trabalho é enviado para a impressora, mas pode não ser impresso ainda.</span><span class="sxs-lookup"><span data-stu-id="9f415-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="9f415-169">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f415-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="9f415-170">STATUS do trabalho \_ \_ retido</span><span class="sxs-lookup"><span data-stu-id="9f415-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="9f415-171">O trabalho foi retido na fila de impressão após a impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="9f415-172">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="9f415-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-173">A prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-173">The job priority.</span></span> <span data-ttu-id="9f415-174">Esse membro pode ser um dos valores a seguir ou no intervalo entre 1 e 99 ( \_ prioridade mínima até a prioridade máxima \_ ).</span><span class="sxs-lookup"><span data-stu-id="9f415-174">This member can be one of the following values, or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="9f415-175">Valor</span><span class="sxs-lookup"><span data-stu-id="9f415-175">Value</span></span>         | <span data-ttu-id="9f415-176">Significado</span><span class="sxs-lookup"><span data-stu-id="9f415-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="9f415-177">\_prioridade mínima</span><span class="sxs-lookup"><span data-stu-id="9f415-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="9f415-178">Prioridade mínima.</span><span class="sxs-lookup"><span data-stu-id="9f415-178">Minimum priority.</span></span> |
| <span data-ttu-id="9f415-179">\_prioridade máxima</span><span class="sxs-lookup"><span data-stu-id="9f415-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="9f415-180">Prioridade máxima.</span><span class="sxs-lookup"><span data-stu-id="9f415-180">Maximum priority.</span></span> |
| <span data-ttu-id="9f415-181">prioridade de DEF. \_</span><span class="sxs-lookup"><span data-stu-id="9f415-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="9f415-182">Prioridade padrão.</span><span class="sxs-lookup"><span data-stu-id="9f415-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9f415-183">**Posição**</span><span class="sxs-lookup"><span data-stu-id="9f415-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-184">A posição do trabalho na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="9f415-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="9f415-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-186">A hora mais antiga em que o trabalho pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="9f415-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="9f415-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-188">A hora mais recente em que o trabalho pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="9f415-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="9f415-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-190">O número de páginas necessárias para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-190">The number of pages required for the job.</span></span> <span data-ttu-id="9f415-191">Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.</span><span class="sxs-lookup"><span data-stu-id="9f415-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-192">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="9f415-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-193">Os quatro bytes inferiores do tamanho, em bytes, do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-193">The lower four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="9f415-194">Consulte também o membro **SizeHigh** abaixo.</span><span class="sxs-lookup"><span data-stu-id="9f415-194">See also the **SizeHigh** member below.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-195">**Enviado**</span><span class="sxs-lookup"><span data-stu-id="9f415-195">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-196">Uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="9f415-196">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="9f415-197">Esse valor de tempo está no formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="9f415-197">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="9f415-198">Você deve convertê-lo em um valor de hora local antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="9f415-198">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="9f415-199">Você pode usar a função [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="9f415-199">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-200">**Hora**</span><span class="sxs-lookup"><span data-stu-id="9f415-200">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-201">O tempo total, em milissegundos, decorrido desde que o trabalho começou a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="9f415-201">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-202">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="9f415-202">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-203">O número de páginas que foram impressas.</span><span class="sxs-lookup"><span data-stu-id="9f415-203">The number of pages that have printed.</span></span> <span data-ttu-id="9f415-204">Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.</span><span class="sxs-lookup"><span data-stu-id="9f415-204">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="9f415-205">**SizeHigh**</span><span class="sxs-lookup"><span data-stu-id="9f415-205">**SizeHigh**</span></span>
</dt> <dd>

<span data-ttu-id="9f415-206">Os quatro bytes mais altos do tamanho, em bytes, do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9f415-206">The higher four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="9f415-207">Consulte também o membro de **tamanho** acima.</span><span class="sxs-lookup"><span data-stu-id="9f415-207">See also the **Size** member above.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f415-208">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f415-208">Remarks</span></span>

<span data-ttu-id="9f415-209">Os monitores de porta que não dão suporte a TrueEndOfJob definirão o trabalho como o status do trabalho \_ \_ impresso imediatamente depois que o trabalho for enviado para a impressora.</span><span class="sxs-lookup"><span data-stu-id="9f415-209">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED immediately after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f415-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f415-210">Requirements</span></span>



| <span data-ttu-id="9f415-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f415-211">Requirement</span></span> | <span data-ttu-id="9f415-212">Valor</span><span class="sxs-lookup"><span data-stu-id="9f415-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f415-213">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f415-213">Minimum supported client</span></span><br/> | <span data-ttu-id="9f415-214">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f415-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9f415-215">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f415-215">Minimum supported server</span></span><br/> | <span data-ttu-id="9f415-216">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f415-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f415-217">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9f415-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f415-218"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f415-218"><dt>Winspool.h</dt></span></span> </dl> |
| <span data-ttu-id="9f415-219">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9f415-219">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9f415-220">Informações do **\_ trabalho \_ \_ 4W** (Unicode) e **\_ info do trabalho \_ \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9f415-220">**\_JOB\_INFO\_4W** (Unicode) and **\_JOB\_INFO\_4A** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9f415-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f415-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f415-222">Impressão</span><span class="sxs-lookup"><span data-stu-id="9f415-222">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9f415-223">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9f415-223">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9f415-224">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="9f415-224">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="9f415-225">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="9f415-225">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="9f415-226">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="9f415-226">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="9f415-227">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="9f415-227">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

