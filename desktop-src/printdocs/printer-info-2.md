---
description: A \_ estrutura informações da impressora \_ 2 especifica informações detalhadas sobre a impressora.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Estrutura de PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506095"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="2c61f-103">Estrutura de informações da impressora \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="2c61f-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="2c61f-104">A **estrutura \_ informações \_ da impressora 2** especifica informações detalhadas sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c61f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c61f-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="2c61f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2c61f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c61f-107">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="2c61f-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica o servidor que controla a impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="2c61f-109">Se essa cadeia de caracteres for **nula**, a impressora será controlada localmente.</span><span class="sxs-lookup"><span data-stu-id="2c61f-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-110">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="2c61f-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-112">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="2c61f-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica o ponto de compartilhamento da impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="2c61f-114">(Essa cadeia de caracteres será usada somente se a impressora \_ \_A constante compartilhada do atributo foi definida para o membro **Attributes** .)</span><span class="sxs-lookup"><span data-stu-id="2c61f-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-115">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="2c61f-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="2c61f-117">Se uma impressora estiver conectada a mais de uma porta, os nomes de cada porta deverão ser separados por vírgulas (por exemplo, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="2c61f-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-118">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="2c61f-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-119">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-120">**pComment**</span><span class="sxs-lookup"><span data-stu-id="2c61f-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-121">Um ponteiro para uma cadeia de caracteres terminada em nulo que fornece uma breve descrição da impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-122">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="2c61f-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-123">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o local físico da impressora (por exemplo, "Bldg.</span><span class="sxs-lookup"><span data-stu-id="2c61f-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="2c61f-124">38, sala 1164 ").</span><span class="sxs-lookup"><span data-stu-id="2c61f-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-125">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="2c61f-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-126">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define dados de impressora padrão, como a orientação do papel e a resolução.</span><span class="sxs-lookup"><span data-stu-id="2c61f-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-127">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="2c61f-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-128">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo usado para criar a página separadora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="2c61f-129">Esta página é usada para separar trabalhos de impressão enviados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-130">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="2c61f-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-131">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão usado pela impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="2c61f-132">Você pode usar a função [**EnumPrintProcessors**](enumprintprocessors.md) para obter uma lista de processadores de impressão instalados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="2c61f-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-133">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="2c61f-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-134">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="2c61f-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="2c61f-135">Você pode usar a função [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para obter uma lista de tipos de dados com suporte por um processador de impressão específico.</span><span class="sxs-lookup"><span data-stu-id="2c61f-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-136">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="2c61f-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-137">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros de processador de impressão padrão.</span><span class="sxs-lookup"><span data-stu-id="2c61f-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-138">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2c61f-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-139">Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para a impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="2c61f-140">Este membro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2c61f-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-141">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="2c61f-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-142">Os atributos da impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-142">The printer attributes.</span></span> <span data-ttu-id="2c61f-143">Esse membro pode ser qualquer combinação razoável dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c61f-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="2c61f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="2c61f-144">Value</span></span>                                   | <span data-ttu-id="2c61f-145">Significado</span><span class="sxs-lookup"><span data-stu-id="2c61f-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c61f-146">atributo de impressora \_ \_ direto</span><span class="sxs-lookup"><span data-stu-id="2c61f-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="2c61f-147">O trabalho é enviado diretamente para a impressora (não é colocado no spool).</span><span class="sxs-lookup"><span data-stu-id="2c61f-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="2c61f-148">o \_ atributo de impressora \_ é \_ concluído \_ primeiro</span><span class="sxs-lookup"><span data-stu-id="2c61f-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="2c61f-149">Se a configuração e a impressora estiverem definidas para impressão durante o spool, todos os trabalhos que concluíram o spool serão agendados para impressão antes dos trabalhos que não concluíram o spool.</span><span class="sxs-lookup"><span data-stu-id="2c61f-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="2c61f-150">atributo de impressora \_ \_ habilitar \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="2c61f-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="2c61f-151">Se definido, **DevQueryPrint** será chamado.</span><span class="sxs-lookup"><span data-stu-id="2c61f-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="2c61f-152">**DevQueryPrint** poderá falhar se as configurações do documento e da impressora não corresponderem.</span><span class="sxs-lookup"><span data-stu-id="2c61f-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="2c61f-153">Definir esse sinalizador faz com que documentos incompatíveis sejam mantidos na fila.</span><span class="sxs-lookup"><span data-stu-id="2c61f-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="2c61f-154">atributo de impressora \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="2c61f-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="2c61f-155">Reservado.</span><span class="sxs-lookup"><span data-stu-id="2c61f-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="2c61f-156">atributo de impressora \_ \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="2c61f-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="2c61f-157">Se definido, os trabalhos são mantidos depois de serem impressos.</span><span class="sxs-lookup"><span data-stu-id="2c61f-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="2c61f-158">Se forem desdefinidas, os trabalhos serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="2c61f-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="2c61f-159">atributo de impressora \_ \_ local</span><span class="sxs-lookup"><span data-stu-id="2c61f-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="2c61f-160">A impressora é uma impressora local.</span><span class="sxs-lookup"><span data-stu-id="2c61f-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="2c61f-161">\_rede de atributos da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="2c61f-162">A impressora é uma conexão de impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="2c61f-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="2c61f-163">atributo de impressora \_ \_ publicado</span><span class="sxs-lookup"><span data-stu-id="2c61f-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="2c61f-164">Indica se a impressora está publicada no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="2c61f-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="2c61f-165">atributo de impressora \_ \_ na fila</span><span class="sxs-lookup"><span data-stu-id="2c61f-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="2c61f-166">Se definido, a impressora coloca em spool e começa a impressão depois que a última página é colocada em spool.</span><span class="sxs-lookup"><span data-stu-id="2c61f-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="2c61f-167">Se não for definido e \_ \_ o atributo de impressora Direct não estiver definido, a impressora spoole e imprime durante o spool.</span><span class="sxs-lookup"><span data-stu-id="2c61f-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="2c61f-168">\_atributo de \_ impressora \_ somente bruto</span><span class="sxs-lookup"><span data-stu-id="2c61f-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="2c61f-169">Indica que apenas trabalhos de impressão de tipo de dados brutos podem ser colocados em spool.</span><span class="sxs-lookup"><span data-stu-id="2c61f-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="2c61f-170">atributo de impressora \_ \_ compartilhado</span><span class="sxs-lookup"><span data-stu-id="2c61f-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="2c61f-171">A impressora está compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2c61f-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="2c61f-172">No Windows XP e versões posteriores do Windows, o valor a seguir também pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="2c61f-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="2c61f-173">Valor</span><span class="sxs-lookup"><span data-stu-id="2c61f-173">Value</span></span>                   | <span data-ttu-id="2c61f-174">Significado</span><span class="sxs-lookup"><span data-stu-id="2c61f-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c61f-175">\_fax de atributo de impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="2c61f-176">Se definido, a impressora é uma impressora de fax.</span><span class="sxs-lookup"><span data-stu-id="2c61f-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="2c61f-177">Isso só pode ser definido pelo [**AddPrinter**](addprinter.md), mas pode ser recuperado por [**EnumPrinters**](enumprinters.md) e [**getprinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="2c61f-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="2c61f-178">No Windows Vista e versões posteriores do Windows, os valores a seguir também podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="2c61f-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="2c61f-179">Valor</span><span class="sxs-lookup"><span data-stu-id="2c61f-179">Value</span></span>                               | <span data-ttu-id="2c61f-180">Significado</span><span class="sxs-lookup"><span data-stu-id="2c61f-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c61f-181">\_ \_ nome amigável do atributo de impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="2c61f-182">Um computador se conectou a essa impressora e deu a ela um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="2c61f-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="2c61f-183">\_computador de atributo de impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="2c61f-184">A impressora é uma conexão por computador.</span><span class="sxs-lookup"><span data-stu-id="2c61f-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="2c61f-185">atributo de impressora \_ \_ enviado por push \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="2c61f-186">A impressora foi instalada usando a política de usuário conexões de push Printer.</span><span class="sxs-lookup"><span data-stu-id="2c61f-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="2c61f-187">computador com o atributo de impressora \_ \_ enviado por push \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="2c61f-188">A impressora foi instalada usando a política de computador conexões de impressora de envio por push.</span><span class="sxs-lookup"><span data-stu-id="2c61f-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="2c61f-189">No Windows Server 2003, o valor a seguir também pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="2c61f-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="2c61f-190">Valor</span><span class="sxs-lookup"><span data-stu-id="2c61f-190">Value</span></span>                  | <span data-ttu-id="2c61f-191">Significado</span><span class="sxs-lookup"><span data-stu-id="2c61f-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="2c61f-192">atributo de impressora \_ \_ TS</span><span class="sxs-lookup"><span data-stu-id="2c61f-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="2c61f-193">Indica que a impressora está atualmente conectada por meio de um servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="2c61f-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2c61f-194">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="2c61f-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-195">Um valor de prioridade que o spooler usa para rotear trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="2c61f-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-196">**Defaultanteriority**</span><span class="sxs-lookup"><span data-stu-id="2c61f-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-197">O valor de prioridade padrão atribuído a cada trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="2c61f-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="2c61f-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-199">A hora mais antiga em que a impressora imprimirá um trabalho.</span><span class="sxs-lookup"><span data-stu-id="2c61f-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="2c61f-200">Esse valor é expresso como minutos decorridos desde 12:00 AM GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="2c61f-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-201">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="2c61f-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-202">A última hora em que a impressora imprimirá um trabalho.</span><span class="sxs-lookup"><span data-stu-id="2c61f-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="2c61f-203">Esse valor é expresso como minutos decorridos desde 12:00 AM GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="2c61f-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-204">**Status**</span><span class="sxs-lookup"><span data-stu-id="2c61f-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-205">O status da impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-205">The printer status.</span></span> <span data-ttu-id="2c61f-206">Esse membro pode ser qualquer combinação razoável dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c61f-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="2c61f-207">Valor</span><span class="sxs-lookup"><span data-stu-id="2c61f-207">Value</span></span>                               | <span data-ttu-id="2c61f-208">Significado</span><span class="sxs-lookup"><span data-stu-id="2c61f-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2c61f-209">STATUS da impressora \_ \_ ocupado</span><span class="sxs-lookup"><span data-stu-id="2c61f-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="2c61f-210">A impressora está ocupada.</span><span class="sxs-lookup"><span data-stu-id="2c61f-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="2c61f-211">porta de status da impressora \_ \_ \_ aberta</span><span class="sxs-lookup"><span data-stu-id="2c61f-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="2c61f-212">A porta da impressora está aberta.</span><span class="sxs-lookup"><span data-stu-id="2c61f-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="2c61f-213">\_erro de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="2c61f-214">A impressora está em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="2c61f-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="2c61f-215">\_inicialização do status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="2c61f-216">A impressora está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="2c61f-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="2c61f-217">STATUS da impressora \_ \_ e/s \_ ativa</span><span class="sxs-lookup"><span data-stu-id="2c61f-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="2c61f-218">A impressora está em um estado de entrada/saída ativo</span><span class="sxs-lookup"><span data-stu-id="2c61f-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="2c61f-219">\_ \_ feed manual de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="2c61f-220">A impressora está em um estado de feed manual.</span><span class="sxs-lookup"><span data-stu-id="2c61f-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="2c61f-221">STATUS da impressora \_ \_ sem \_ toner</span><span class="sxs-lookup"><span data-stu-id="2c61f-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="2c61f-222">A impressora está sem toner.</span><span class="sxs-lookup"><span data-stu-id="2c61f-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="2c61f-223">STATUS da impressora \_ \_ não \_ disponível</span><span class="sxs-lookup"><span data-stu-id="2c61f-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="2c61f-224">A impressora não está disponível para impressão.</span><span class="sxs-lookup"><span data-stu-id="2c61f-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="2c61f-225">STATUS da impressora \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="2c61f-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="2c61f-226">A impressora está offline.</span><span class="sxs-lookup"><span data-stu-id="2c61f-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="2c61f-227">\_status \_ da impressora fora \_ da \_ memória</span><span class="sxs-lookup"><span data-stu-id="2c61f-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="2c61f-228">A impressora ficou sem memória.</span><span class="sxs-lookup"><span data-stu-id="2c61f-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="2c61f-229">bandeja de saída de status da impressora \_ \_ \_ \_ cheia</span><span class="sxs-lookup"><span data-stu-id="2c61f-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="2c61f-230">O compartimento de saída da impressora está cheio.</span><span class="sxs-lookup"><span data-stu-id="2c61f-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="2c61f-231">\_ \_ apontador de página de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="2c61f-232">A impressora não pode imprimir a página atual.</span><span class="sxs-lookup"><span data-stu-id="2c61f-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="2c61f-233">\_ \_ emperramento de papel do status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="2c61f-234">O papel está emperrado na impressora</span><span class="sxs-lookup"><span data-stu-id="2c61f-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="2c61f-235">\_saída do status da impressora \_ \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="2c61f-236">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="2c61f-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="2c61f-237">\_problema de \_ papel do status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="2c61f-238">A impressora tem um problema de papel.</span><span class="sxs-lookup"><span data-stu-id="2c61f-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="2c61f-239">STATUS da impressora em \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="2c61f-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="2c61f-240">A impressora está em pausa.</span><span class="sxs-lookup"><span data-stu-id="2c61f-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="2c61f-241">\_exclusão de status \_ da impressora pendente \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="2c61f-242">A impressora está sendo excluída.</span><span class="sxs-lookup"><span data-stu-id="2c61f-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="2c61f-243">\_economia de \_ energia de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="2c61f-244">A impressora está no modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="2c61f-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="2c61f-245">\_impressão de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="2c61f-246">A impressora está imprimindo.</span><span class="sxs-lookup"><span data-stu-id="2c61f-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="2c61f-247">\_processamento de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="2c61f-248">A impressora está processando um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="2c61f-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="2c61f-249">servidor de status de impressora \_ \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="2c61f-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="2c61f-250">O status da impressora é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2c61f-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="2c61f-251">\_toner de status da impressora \_ \_ baixo</span><span class="sxs-lookup"><span data-stu-id="2c61f-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="2c61f-252">A impressora está com pouco toner.</span><span class="sxs-lookup"><span data-stu-id="2c61f-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="2c61f-253">\_status da \_ impressora \_ intervenção do usuário</span><span class="sxs-lookup"><span data-stu-id="2c61f-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="2c61f-254">A impressora tem um erro que exige que o usuário faça algo.</span><span class="sxs-lookup"><span data-stu-id="2c61f-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="2c61f-255">STATUS da impressora \_ \_ aguardando</span><span class="sxs-lookup"><span data-stu-id="2c61f-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="2c61f-256">A impressora está aguardando.</span><span class="sxs-lookup"><span data-stu-id="2c61f-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="2c61f-257">STATUS da impressora \_ \_ aquecendo \_</span><span class="sxs-lookup"><span data-stu-id="2c61f-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="2c61f-258">A impressora está em preparação.</span><span class="sxs-lookup"><span data-stu-id="2c61f-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="2c61f-259">**cJobs**</span><span class="sxs-lookup"><span data-stu-id="2c61f-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-260">O número de trabalhos de impressão que foram enfileirados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="2c61f-261">**AveragePPM**</span><span class="sxs-lookup"><span data-stu-id="2c61f-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="2c61f-262">O número médio de páginas por minuto que foram impressas na impressora.</span><span class="sxs-lookup"><span data-stu-id="2c61f-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c61f-263">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c61f-263">Requirements</span></span>



| <span data-ttu-id="2c61f-264">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c61f-264">Requirement</span></span> | <span data-ttu-id="2c61f-265">Valor</span><span class="sxs-lookup"><span data-stu-id="2c61f-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c61f-266">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c61f-266">Minimum supported client</span></span><br/> | <span data-ttu-id="2c61f-267">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c61f-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2c61f-268">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c61f-268">Minimum supported server</span></span><br/> | <span data-ttu-id="2c61f-269">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c61f-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2c61f-270">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c61f-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c61f-271"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c61f-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2c61f-272">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2c61f-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2c61f-273">Informações de **\_ impressora \_ \_ 2W** (Unicode) e **\_ informações de impressora \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c61f-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="2c61f-274">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c61f-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c61f-275">Impressão</span><span class="sxs-lookup"><span data-stu-id="2c61f-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2c61f-276">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="2c61f-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2c61f-277">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="2c61f-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="2c61f-278">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="2c61f-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="2c61f-279">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2c61f-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="2c61f-280">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="2c61f-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="2c61f-281">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="2c61f-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="2c61f-282">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="2c61f-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

