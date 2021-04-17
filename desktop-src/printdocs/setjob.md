---
description: A função SetJob pausa, retoma, cancela ou reinicia um trabalho de impressão em uma impressora especificada. Você também pode usar a função SetJob para definir parâmetros de trabalho de impressão, como a prioridade do trabalho de impressão e o nome do documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Função SetJob (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780070"
---
# <a name="setjob-function"></a><span data-ttu-id="95bdb-104">Função SetJob</span><span class="sxs-lookup"><span data-stu-id="95bdb-104">SetJob function</span></span>

<span data-ttu-id="95bdb-105">A função **SetJob** pausa, retoma, cancela ou reinicia um trabalho de impressão em uma impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="95bdb-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="95bdb-106">Você também pode usar a função **SetJob** para definir parâmetros de trabalho de impressão, como a prioridade do trabalho de impressão e o nome do documento.</span><span class="sxs-lookup"><span data-stu-id="95bdb-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="95bdb-107">Você pode usar a função **SetJob** para fornecer um comando para um trabalho de impressão ou para definir os parâmetros do trabalho de impressão ou para fazer ambos na mesma chamada.</span><span class="sxs-lookup"><span data-stu-id="95bdb-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="95bdb-108">O valor do parâmetro *Command* não afeta como a função usa os parâmetros *Level* e *pJob* .</span><span class="sxs-lookup"><span data-stu-id="95bdb-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="95bdb-109">Além disso, você pode usar **SetJob** com [**informações de trabalho \_ \_ 3**](job-info-3.md) para vincular um conjunto de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="95bdb-110">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="95bdb-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bdb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95bdb-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="95bdb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95bdb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bdb-113">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bdb-114">Um identificador para o objeto de impressora de interesse.</span><span class="sxs-lookup"><span data-stu-id="95bdb-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="95bdb-115">Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="95bdb-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="95bdb-116">*JobID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bdb-117">Identificador que especifica o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="95bdb-118">Você Obtém um identificador de trabalho de impressão chamando a função [**AddJob**](addjob.md) ou a função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="95bdb-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="95bdb-119">Se o parâmetro *Level* for definido como 3, o parâmetro *JobID* deverá corresponder ao membro **JobID** da estrutura [**info do trabalho \_ \_ 3**](job-info-3.md) apontada por *pJob*</span><span class="sxs-lookup"><span data-stu-id="95bdb-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="95bdb-120">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bdb-121">O tipo de estrutura de informações do trabalho apontado pelo parâmetro *pJob* .</span><span class="sxs-lookup"><span data-stu-id="95bdb-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="95bdb-122">**Todas as versões do Windows**: você pode definir o parâmetro *Level* como 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="95bdb-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="95bdb-123">Quando você define *nível* como 0, *PJob* deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="95bdb-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="95bdb-124">Use esses valores quando você não estiver definindo nenhum parâmetro de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="95bdb-125">Você também pode definir o parâmetro *Level* como 3.</span><span class="sxs-lookup"><span data-stu-id="95bdb-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="95bdb-126">A partir do **Windows Vista**: você também pode definir o parâmetro *Level* como 4.</span><span class="sxs-lookup"><span data-stu-id="95bdb-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="95bdb-127">*pJob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bdb-128">Um ponteiro para uma estrutura que define os parâmetros do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="95bdb-129">**Todas as versões do Windows**: *pJob* podem apontar para uma estrutura de [**informações de trabalho \_ \_ 1**](job-info-1.md) ou de [**\_ informações \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="95bdb-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="95bdb-130">*pJob* também pode apontar para uma estrutura de [**informações de trabalho \_ \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="95bdb-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="95bdb-131">Você deve ter **acesso ao trabalho \_ \_ administrar** permissão de acesso para os trabalhos especificados pelos membros **JobID** e **NextJobId** da **estrutura \_ informações \_ do trabalho 3** .</span><span class="sxs-lookup"><span data-stu-id="95bdb-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="95bdb-132">A partir do **Windows Vista**: o *pJob* também pode apontar para uma estrutura de [**informações do trabalho \_ \_ 4**](job-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="95bdb-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="95bdb-133">Se o parâmetro *Level* for 0, *PJob* deverá ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="95bdb-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95bdb-134">*Comando* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bdb-135">A operação de trabalho de impressão a ser executada.</span><span class="sxs-lookup"><span data-stu-id="95bdb-135">The print job operation to perform.</span></span> <span data-ttu-id="95bdb-136">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="95bdb-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="95bdb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="95bdb-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="95bdb-138">Significado</span><span class="sxs-lookup"><span data-stu-id="95bdb-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="95bdb-139"><dt>**cancelamento do controle de trabalho \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="95bdb-140">Não use.</span><span class="sxs-lookup"><span data-stu-id="95bdb-140">Do not use.</span></span> <span data-ttu-id="95bdb-141">Para excluir um trabalho de impressão, use a **\_ \_ exclusão de controle de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="95bdb-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="95bdb-142"><dt>**\_pausa de controle de trabalho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="95bdb-143">Pausar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="95bdb-144"><dt>**reinicialização do controle de trabalho \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="95bdb-145">Reinicie o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-145">Restart the print job.</span></span> <span data-ttu-id="95bdb-146">Um trabalho só poderá ser reiniciado se tiver sido impresso.</span><span class="sxs-lookup"><span data-stu-id="95bdb-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="95bdb-147"><dt>**retomada do controle de trabalho \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="95bdb-148">Retomar um trabalho de impressão em pausa.</span><span class="sxs-lookup"><span data-stu-id="95bdb-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="95bdb-149"><dt>**\_exclusão de controle de trabalho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="95bdb-150">Exclua o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="95bdb-151"><dt>**\_controle \_ de trabalho enviado \_ para a \_ impressora**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="95bdb-152">Usado por monitores de porta para finalizar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="95bdb-153"><dt>**\_última página de controle de trabalho \_ \_ \_ ejetada**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="95bdb-154">Usado por monitores de idioma para finalizar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="95bdb-155"><dt>**\_retenção de controle de trabalho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="95bdb-156">**Windows Vista e posterior**: manter o trabalho na fila depois que ele for impresso.</span><span class="sxs-lookup"><span data-stu-id="95bdb-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="95bdb-157"><dt>**\_versão de controle de trabalho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="95bdb-158">**Windows Vista e posterior**: Libere o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="95bdb-159">Você pode usar a mesma chamada para a função **SetJob** para definir parâmetros de trabalho de impressão e para dar um comando a um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="95bdb-160">Portanto, o *comando* não precisa ser 0 se você estiver definindo parâmetros de trabalho de impressão, embora possa ser.</span><span class="sxs-lookup"><span data-stu-id="95bdb-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bdb-161">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95bdb-161">Return value</span></span>

<span data-ttu-id="95bdb-162">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="95bdb-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="95bdb-163">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="95bdb-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="95bdb-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="95bdb-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95bdb-165">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="95bdb-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="95bdb-166">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="95bdb-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="95bdb-167">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="95bdb-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="95bdb-168">Você pode usar a função **SetJob** para definir vários parâmetros de trabalho de impressão fornecendo um ponteiro para uma estrutura [**informações de trabalho \_ \_ 1**](job-info-1.md), [**informações do trabalho \_ \_ 2**](job-info-2.md), [**informações do trabalho \_ \_ 3**](job-info-3.md)ou informações do trabalho [**\_ \_ 4**](job-info-4.md) que contém os dados necessários.</span><span class="sxs-lookup"><span data-stu-id="95bdb-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="95bdb-169">Para remover ou excluir todos os trabalhos de impressão de uma impressora específica, chame a função [**Setprintr**](setprinter.md) com seu parâmetro de *comando* definido **como \_ \_ limpeza de controle da impressora**.</span><span class="sxs-lookup"><span data-stu-id="95bdb-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="95bdb-170">Os seguintes membros de uma [**estrutura \_ informações \_ de trabalho 1**](job-info-1.md), [**\_ informações sobre o trabalho \_ 2**](job-info-2.md)ou [**informações do trabalho \_ \_ 4**](job-info-4.md) são ignorados em uma chamada para **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **tamanho**, **enviado**, **hora** e **TotalPages**.</span><span class="sxs-lookup"><span data-stu-id="95bdb-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="95bdb-171">Você deve ter **\_ acesso à impressora \_ administrar** permissão de acesso para uma impressora a fim de alterar a posição de um trabalho de impressão na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="95bdb-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="95bdb-172">Se você não quiser definir a posição de um trabalho de impressão na fila de impressão, defina o membro **posição** da estrutura informações do [**trabalho \_ \_ 1**](job-info-1.md), [**informações do \_ trabalho \_ 2**](job-info-2.md)ou [**informações do \_ trabalho \_ 4**](job-info-4.md) para a **posição do trabalho \_ \_ não especificado**.</span><span class="sxs-lookup"><span data-stu-id="95bdb-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="95bdb-173">Use a função **SetJob** com a estrutura [**informações do trabalho \_ \_ 3**](job-info-3.md) para vincular um conjunto de trabalhos de impressão (também conhecido como cadeia).</span><span class="sxs-lookup"><span data-stu-id="95bdb-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="95bdb-174">Isso é útil em situações em que um único documento consiste em várias partes que você deseja renderizar separadamente.</span><span class="sxs-lookup"><span data-stu-id="95bdb-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="95bdb-175">Para imprimir trabalhos A, B, C e D em ordem, chame **SetJob** com as [**informações do trabalho \_ \_ 4**](job-info-4.md) para vincular a a B, B a c e c a D.</span><span class="sxs-lookup"><span data-stu-id="95bdb-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="95bdb-176">Se você vincular trabalhos de impressão, observe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="95bdb-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="95bdb-177">Os trabalhos podem ser adicionados ao início ou ao fim de uma cadeia.</span><span class="sxs-lookup"><span data-stu-id="95bdb-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="95bdb-178">Todos os trabalhos na cadeia devem ter o mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="95bdb-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="95bdb-179">A cadeia deve estar completamente vinculada antes do início do spool, caso contrário, o spooler pode imprimir e excluir trabalhos em spool antes de vincular todos eles.</span><span class="sxs-lookup"><span data-stu-id="95bdb-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="95bdb-180">Há duas maneiras de manter a cadeia de impressão prematuramente:</span><span class="sxs-lookup"><span data-stu-id="95bdb-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="95bdb-181">Pause o primeiro trabalho na cadeia até que a cadeia seja completamente vinculada.</span><span class="sxs-lookup"><span data-stu-id="95bdb-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="95bdb-182">O estado de pausa do primeiro trabalho governa o estado de todos os trabalhos na cadeia.</span><span class="sxs-lookup"><span data-stu-id="95bdb-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="95bdb-183">Mantenha o primeiro trabalho incompleto, ou seja, não chame [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) ou [**ScheduleJob**](schedulejob.md) para o primeiro trabalho.</span><span class="sxs-lookup"><span data-stu-id="95bdb-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="95bdb-184">No entanto, se ' Imprimir durante o spool ' estiver habilitado (o padrão), esse método bloqueará a porta enquanto a cadeia for criada, o que também impedirá a impressão de trabalhos não relacionados.</span><span class="sxs-lookup"><span data-stu-id="95bdb-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="95bdb-185">O aplicativo deve lidar com o caso em que o usuário exclui um trabalho na cadeia antes de a cadeia terminar de ser impressa.</span><span class="sxs-lookup"><span data-stu-id="95bdb-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="95bdb-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **um \_ parâmetro inválido** quando um JobID não existe.</span><span class="sxs-lookup"><span data-stu-id="95bdb-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bdb-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95bdb-187">Requirements</span></span>



| <span data-ttu-id="95bdb-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="95bdb-188">Requirement</span></span> | <span data-ttu-id="95bdb-189">Valor</span><span class="sxs-lookup"><span data-stu-id="95bdb-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95bdb-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95bdb-190">Minimum supported client</span></span><br/> | <span data-ttu-id="95bdb-191">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="95bdb-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95bdb-192">Minimum supported server</span></span><br/> | <span data-ttu-id="95bdb-193">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95bdb-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="95bdb-194">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95bdb-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="95bdb-195"><dt>WinSpool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="95bdb-196">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95bdb-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="95bdb-197"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="95bdb-198">DLL</span><span class="sxs-lookup"><span data-stu-id="95bdb-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95bdb-199"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="95bdb-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="95bdb-200">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="95bdb-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95bdb-201">**SetJobW** (Unicode) e **SetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="95bdb-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="95bdb-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="95bdb-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bdb-203">Impressão</span><span class="sxs-lookup"><span data-stu-id="95bdb-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="95bdb-204">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="95bdb-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="95bdb-205">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="95bdb-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="95bdb-206">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="95bdb-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="95bdb-207">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="95bdb-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="95bdb-208">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="95bdb-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="95bdb-209">**Informações do trabalho \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="95bdb-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="95bdb-210">**Informações do trabalho \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="95bdb-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="95bdb-211">**Informações do trabalho \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="95bdb-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="95bdb-212">**Informações do trabalho \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="95bdb-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

