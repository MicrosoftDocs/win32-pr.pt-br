---
description: A \_ estrutura informações da impressora \_ 5 especifica informações detalhadas sobre a impressora.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Estrutura de PRINTER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768397"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="5ae7c-103">Estrutura de informações da impressora \_ \_ 5</span><span class="sxs-lookup"><span data-stu-id="5ae7c-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="5ae7c-104">A **estrutura \_ informações \_ da impressora 5** especifica informações detalhadas sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae7c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ae7c-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="5ae7c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5ae7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ae7c-107">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="5ae7c-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="5ae7c-109">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="5ae7c-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="5ae7c-111">Se uma impressora estiver conectada a mais de uma porta, os nomes de cada porta deverão ser separados por vírgulas (por exemplo, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="5ae7c-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="5ae7c-112">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="5ae7c-113">Os atributos da impressora.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-113">The printer attributes.</span></span> <span data-ttu-id="5ae7c-114">Esse membro pode ser qualquer combinação razoável dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="5ae7c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5ae7c-115">Value</span></span>                                   | <span data-ttu-id="5ae7c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5ae7c-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7c-117">atributo de impressora \_ \_ direto</span><span class="sxs-lookup"><span data-stu-id="5ae7c-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="5ae7c-118">O trabalho é enviado diretamente para a impressora (não é colocado no spool).</span><span class="sxs-lookup"><span data-stu-id="5ae7c-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="5ae7c-119">o \_ atributo de impressora \_ é \_ concluído \_ primeiro</span><span class="sxs-lookup"><span data-stu-id="5ae7c-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="5ae7c-120">Se a configuração e a impressora estiverem definidas para impressão durante o spool, todos os trabalhos que concluíram o spool serão agendados para impressão antes dos trabalhos que não concluíram o spool.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="5ae7c-121">atributo de impressora \_ \_ habilitar \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="5ae7c-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="5ae7c-122">Se definido, **DevQueryPrint** será chamado.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="5ae7c-123">**DevQueryPrint** poderá falhar se as configurações do documento e da impressora não corresponderem.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="5ae7c-124">Definir esse sinalizador faz com que documentos incompatíveis sejam mantidos na fila.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="5ae7c-125">atributo de impressora \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="5ae7c-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="5ae7c-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="5ae7c-127">atributo de impressora \_ \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="5ae7c-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="5ae7c-128">Se definido, os trabalhos são mantidos depois de serem impressos.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="5ae7c-129">Se forem desdefinidas, os trabalhos serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="5ae7c-130">atributo de impressora \_ \_ local</span><span class="sxs-lookup"><span data-stu-id="5ae7c-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="5ae7c-131">A impressora é uma impressora local.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="5ae7c-132">\_rede de atributos da impressora \_</span><span class="sxs-lookup"><span data-stu-id="5ae7c-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="5ae7c-133">A impressora é uma conexão de impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="5ae7c-134">atributo de impressora \_ \_ publicado</span><span class="sxs-lookup"><span data-stu-id="5ae7c-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="5ae7c-135">Indica se a impressora está publicada no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="5ae7c-136">atributo de impressora \_ \_ na fila</span><span class="sxs-lookup"><span data-stu-id="5ae7c-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="5ae7c-137">Se definido, a impressora coloca em spool e começa a impressão depois que a última página é colocada em spool.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="5ae7c-138">Se não for definido e \_ \_ o atributo de impressora Direct não estiver definido, a impressora spoole e imprime durante o spool.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="5ae7c-139">\_atributo de \_ impressora \_ somente bruto</span><span class="sxs-lookup"><span data-stu-id="5ae7c-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="5ae7c-140">Indica que apenas trabalhos de impressão de tipo de dados brutos podem ser colocados em spool.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="5ae7c-141">atributo de impressora \_ \_ compartilhado</span><span class="sxs-lookup"><span data-stu-id="5ae7c-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="5ae7c-142">A impressora está compartilhada.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="5ae7c-143">No Windows XP e versões posteriores do Windows, o valor a seguir também pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="5ae7c-144">Valor</span><span class="sxs-lookup"><span data-stu-id="5ae7c-144">Value</span></span>                   | <span data-ttu-id="5ae7c-145">Significado</span><span class="sxs-lookup"><span data-stu-id="5ae7c-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7c-146">\_fax de atributo de impressora \_</span><span class="sxs-lookup"><span data-stu-id="5ae7c-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="5ae7c-147">Se definido, a impressora é uma impressora de fax.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="5ae7c-148">Isso só pode ser definido pelo [**AddPrinter**](addprinter.md), mas pode ser recuperado por [**EnumPrinters**](enumprinters.md) e [**getprinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5ae7c-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="5ae7c-149">No Windows Vista e versões posteriores do Windows, os valores a seguir também podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="5ae7c-150">Valor</span><span class="sxs-lookup"><span data-stu-id="5ae7c-150">Value</span></span>                               | <span data-ttu-id="5ae7c-151">Significado</span><span class="sxs-lookup"><span data-stu-id="5ae7c-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7c-152">\_ \_ nome amigável do atributo de impressora \_</span><span class="sxs-lookup"><span data-stu-id="5ae7c-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="5ae7c-153">Um computador se conectou a essa impressora e deu a ela um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="5ae7c-154">\_computador de atributo de impressora \_</span><span class="sxs-lookup"><span data-stu-id="5ae7c-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="5ae7c-155">A impressora é uma conexão por computador.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="5ae7c-156">atributo de impressora \_ \_ enviado por push \_</span><span class="sxs-lookup"><span data-stu-id="5ae7c-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="5ae7c-157">A impressora foi instalada usando a política de usuário conexões de push Printer.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="5ae7c-158">computador com o atributo de impressora \_ \_ enviado por push \_</span><span class="sxs-lookup"><span data-stu-id="5ae7c-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="5ae7c-159">A impressora foi instalada usando a política de computador conexões de impressora de envio por push.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5ae7c-160">**DeviceNotSelectedTimeout**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="5ae7c-161">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ae7c-162">**TransmissionRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="5ae7c-163">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="5ae7c-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ae7c-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae7c-164">Requirements</span></span>



| <span data-ttu-id="5ae7c-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae7c-165">Requirement</span></span> | <span data-ttu-id="5ae7c-166">Valor</span><span class="sxs-lookup"><span data-stu-id="5ae7c-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7c-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ae7c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae7c-168">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ae7c-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ae7c-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ae7c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae7c-170">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ae7c-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ae7c-171">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5ae7c-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ae7c-172"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae7c-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5ae7c-173">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5ae7c-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5ae7c-174">**\_ Informações de impressora \_ \_ 5W** (Unicode) e **\_ informações de impressora \_ \_ 5a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5ae7c-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="5ae7c-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ae7c-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae7c-176">Impressão</span><span class="sxs-lookup"><span data-stu-id="5ae7c-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-177">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="5ae7c-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-178">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-179">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-180">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-181">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-182">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-183">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="5ae7c-184">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="5ae7c-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




