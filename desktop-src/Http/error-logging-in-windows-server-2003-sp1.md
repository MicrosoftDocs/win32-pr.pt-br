---
title: Log de erros no Windows Server 2003 SP1
description: Log de erros no Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Log de erros no Windows Server 2003 com Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/14/2019
ms.locfileid: "103638848"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="0833a-104">Log de erros no Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="0833a-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="0833a-105">Adição de cabeçalhos de estilo W3C</span><span class="sxs-lookup"><span data-stu-id="0833a-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="0833a-106">A partir do Windows Server 2003 com Service Pack 1 (SP1), o log de erros da API do servidor HTTP inclui cabeçalhos de estilo W3C que permitem que os arquivos de log sejam analisados usando analisadores de log padrão.</span><span class="sxs-lookup"><span data-stu-id="0833a-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="0833a-107">O modelo mostrado abaixo lista todos os campos que podem ser registrados no arquivo de log de erros http.</span><span class="sxs-lookup"><span data-stu-id="0833a-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="0833a-108">Registrando campos adicionais</span><span class="sxs-lookup"><span data-stu-id="0833a-108">Logging Additional Fields</span></span>

<span data-ttu-id="0833a-109">O log de erros HTTP foi estendido para incluir mais nove campos para registrar dados sobre falhas que ocorrem.</span><span class="sxs-lookup"><span data-stu-id="0833a-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="0833a-110">Os novos campos de erro são listados abaixo:</span><span class="sxs-lookup"><span data-stu-id="0833a-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="0833a-111">Nome do computador do servidor \[ S-computername\]</span><span class="sxs-lookup"><span data-stu-id="0833a-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="0833a-112">Agente \[ do usuário cs ( \_ agente do usuário)\]</span><span class="sxs-lookup"><span data-stu-id="0833a-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="0833a-113">\[Cs de cookie (cookie)\]</span><span class="sxs-lookup"><span data-stu-id="0833a-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="0833a-114">\[cs (referenciador) do referenciador\]</span><span class="sxs-lookup"><span data-stu-id="0833a-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="0833a-115">Nome do host \[ cs-host\]</span><span class="sxs-lookup"><span data-stu-id="0833a-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="0833a-116">Bytes recebidos pelo servidor \[ SC-bytes\]</span><span class="sxs-lookup"><span data-stu-id="0833a-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="0833a-117">Bytes recebidos e processados pelo servidor \[ cs-bytes\]</span><span class="sxs-lookup"><span data-stu-id="0833a-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="0833a-118">Tempo necessário para processar o tempo de solicitação \[ -Obtido\]</span><span class="sxs-lookup"><span data-stu-id="0833a-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="0833a-119">Queue-Name (reservado para IIS) \[ S-QueueName\]</span><span class="sxs-lookup"><span data-stu-id="0833a-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="0833a-120">Selecionando arquivos para fazer logon no arquivo de log de erros HTTP</span><span class="sxs-lookup"><span data-stu-id="0833a-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="0833a-121">A chave do registro **ErrorLoggingFields** foi adicionada para controlar os campos registrados no log de erros http.</span><span class="sxs-lookup"><span data-stu-id="0833a-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="0833a-122">Esses valores de registro estão localizados sob uma \\ chave de parâmetros http localizada em:</span><span class="sxs-lookup"><span data-stu-id="0833a-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="0833a-123">O valor do registro **ErrorLoggingFields** é um valor DWORD que contém valores de bits para cada um dos campos que podem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="0833a-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="0833a-124">Para habilitar o registro em log de um campo específico, defina seu valor de bit correspondente como 1 e reinicie o serviço HTTP.</span><span class="sxs-lookup"><span data-stu-id="0833a-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="0833a-125">Para desabilitar o registro em log, defina o valor de bit como 0.</span><span class="sxs-lookup"><span data-stu-id="0833a-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="0833a-126">Para configurar vários campos, use um ou mais bits de valores individuais.</span><span class="sxs-lookup"><span data-stu-id="0833a-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="0833a-127">Por exemplo, para ativar os campos de registro em log de cookies e referenciais, o valor deve ser 0x00020000 \| 0x00040000 = 0x00060000.</span><span class="sxs-lookup"><span data-stu-id="0833a-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="0833a-128">Se a chave do registro **ErrorLoggingFields** estiver ausente, os campos padrão serão registrados.</span><span class="sxs-lookup"><span data-stu-id="0833a-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="0833a-129">O valor de **ErrorLoggingFields** para registrar os campos padrão é 0x7c884c7.</span><span class="sxs-lookup"><span data-stu-id="0833a-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="0833a-130">Para habilitar o registro em log para todos os campos mostrados na tabela abaixo, defina o valor como 0x7dff4e7.</span><span class="sxs-lookup"><span data-stu-id="0833a-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="0833a-131">Os campos de log de erros são listados na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="0833a-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="0833a-132">Campo de log</span><span class="sxs-lookup"><span data-stu-id="0833a-132">Log field</span></span>            | <span data-ttu-id="0833a-133">Registrado por padrão</span><span class="sxs-lookup"><span data-stu-id="0833a-133">Logged by default</span></span> | <span data-ttu-id="0833a-134">Valor de bit</span><span class="sxs-lookup"><span data-stu-id="0833a-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="0833a-135">Data</span><span class="sxs-lookup"><span data-stu-id="0833a-135">Date</span></span>                 | <span data-ttu-id="0833a-136">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-136">Yes</span></span>               | <span data-ttu-id="0833a-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0833a-137">0x00000001</span></span> |
| <span data-ttu-id="0833a-138">Hora</span><span class="sxs-lookup"><span data-stu-id="0833a-138">Time</span></span>                 | <span data-ttu-id="0833a-139">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-139">Yes</span></span>               | <span data-ttu-id="0833a-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0833a-140">0x00000002</span></span> |
| <span data-ttu-id="0833a-141">Nome do computador servidor</span><span class="sxs-lookup"><span data-stu-id="0833a-141">Server Computer Name</span></span> | <span data-ttu-id="0833a-142">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-142">No</span></span>                | <span data-ttu-id="0833a-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="0833a-143">0x00000020</span></span> |
| <span data-ttu-id="0833a-144">Endereço IP do Cliente</span><span class="sxs-lookup"><span data-stu-id="0833a-144">Client IP Address</span></span>    | <span data-ttu-id="0833a-145">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-145">Yes</span></span>               | <span data-ttu-id="0833a-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0833a-146">0x00000004</span></span> |
| <span data-ttu-id="0833a-147">Porta do cliente</span><span class="sxs-lookup"><span data-stu-id="0833a-147">Client Port</span></span>          | <span data-ttu-id="0833a-148">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-148">Yes</span></span>               | <span data-ttu-id="0833a-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="0833a-149">0x00400000</span></span> |
| <span data-ttu-id="0833a-150">Endereço IP do servidor</span><span class="sxs-lookup"><span data-stu-id="0833a-150">Server IP Address</span></span>    | <span data-ttu-id="0833a-151">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-151">Yes</span></span>               | <span data-ttu-id="0833a-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="0833a-152">0x00000040</span></span> |
| <span data-ttu-id="0833a-153">Porta do servidor</span><span class="sxs-lookup"><span data-stu-id="0833a-153">Server Port</span></span>          | <span data-ttu-id="0833a-154">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-154">Yes</span></span>               | <span data-ttu-id="0833a-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="0833a-155">0x00008000</span></span> |
| <span data-ttu-id="0833a-156">Versão do protocolo</span><span class="sxs-lookup"><span data-stu-id="0833a-156">Protocol Version</span></span>     | <span data-ttu-id="0833a-157">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-157">Yes</span></span>               | <span data-ttu-id="0833a-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="0833a-158">0x00080000</span></span> |
| <span data-ttu-id="0833a-159">Método</span><span class="sxs-lookup"><span data-stu-id="0833a-159">Method</span></span>               | <span data-ttu-id="0833a-160">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-160">Yes</span></span>               | <span data-ttu-id="0833a-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="0833a-161">0x00000080</span></span> |
| <span data-ttu-id="0833a-162">URI</span><span class="sxs-lookup"><span data-stu-id="0833a-162">URI</span></span>                  | <span data-ttu-id="0833a-163">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-163">Yes</span></span>               | <span data-ttu-id="0833a-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="0833a-164">0x00800000</span></span> |
| <span data-ttu-id="0833a-165">Agente do usuário</span><span class="sxs-lookup"><span data-stu-id="0833a-165">User Agent</span></span>           | <span data-ttu-id="0833a-166">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-166">No</span></span>                | <span data-ttu-id="0833a-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="0833a-167">0x00010000</span></span> |
| <span data-ttu-id="0833a-168">Cookie</span><span class="sxs-lookup"><span data-stu-id="0833a-168">Cookie</span></span>               | <span data-ttu-id="0833a-169">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-169">No</span></span>                | <span data-ttu-id="0833a-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="0833a-170">0x00020000</span></span> |
| <span data-ttu-id="0833a-171">referenciador</span><span class="sxs-lookup"><span data-stu-id="0833a-171">referrer</span></span>             | <span data-ttu-id="0833a-172">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-172">No</span></span>                | <span data-ttu-id="0833a-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="0833a-173">0x00040000</span></span> |
| <span data-ttu-id="0833a-174">Host</span><span class="sxs-lookup"><span data-stu-id="0833a-174">Host</span></span>                 | <span data-ttu-id="0833a-175">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-175">No</span></span>                | <span data-ttu-id="0833a-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="0833a-176">0x00100000</span></span> |
| <span data-ttu-id="0833a-177">Status do protocolo</span><span class="sxs-lookup"><span data-stu-id="0833a-177">Protocol Status</span></span>      | <span data-ttu-id="0833a-178">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-178">Yes</span></span>               | <span data-ttu-id="0833a-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="0833a-179">0x00000400</span></span> |
| <span data-ttu-id="0833a-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="0833a-180">SC-Bytes</span></span>             | <span data-ttu-id="0833a-181">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-181">No</span></span>                | <span data-ttu-id="0833a-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="0833a-182">0x00001000</span></span> |
| <span data-ttu-id="0833a-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="0833a-183">CS-Bytes</span></span>             | <span data-ttu-id="0833a-184">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-184">No</span></span>                | <span data-ttu-id="0833a-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="0833a-185">0x00002000</span></span> |
| <span data-ttu-id="0833a-186">Tempo decorrido</span><span class="sxs-lookup"><span data-stu-id="0833a-186">Time Taken</span></span>           | <span data-ttu-id="0833a-187">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-187">No</span></span>                | <span data-ttu-id="0833a-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="0833a-188">0x00004000</span></span> |
| <span data-ttu-id="0833a-189">SiteId</span><span class="sxs-lookup"><span data-stu-id="0833a-189">SiteId</span></span>               | <span data-ttu-id="0833a-190">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-190">Yes</span></span>               | <span data-ttu-id="0833a-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="0833a-191">0x01000000</span></span> |
| <span data-ttu-id="0833a-192">Frase do motivo</span><span class="sxs-lookup"><span data-stu-id="0833a-192">Reason Phrase</span></span>        | <span data-ttu-id="0833a-193">Sim</span><span class="sxs-lookup"><span data-stu-id="0833a-193">Yes</span></span>               | <span data-ttu-id="0833a-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="0833a-194">0x02000000</span></span> |
| <span data-ttu-id="0833a-195">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="0833a-195">Queue Name</span></span>           | <span data-ttu-id="0833a-196">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-196">No</span></span>                | <span data-ttu-id="0833a-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="0833a-197">0x04000000</span></span> |
| <span data-ttu-id="0833a-198">ID do fluxo</span><span class="sxs-lookup"><span data-stu-id="0833a-198">Stream Id</span></span>            | <span data-ttu-id="0833a-199">Não</span><span class="sxs-lookup"><span data-stu-id="0833a-199">No</span></span>                | <span data-ttu-id="0833a-200">0x????????</span><span class="sxs-lookup"><span data-stu-id="0833a-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="0833a-201">Substituição de data e hora</span><span class="sxs-lookup"><span data-stu-id="0833a-201">Time and Date Rollover</span></span>

<span data-ttu-id="0833a-202">Por padrão, um novo arquivo de log de erros HTTP é criado (substituição de arquivo com prazo) quando o arquivo de log atual atinge um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="0833a-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="0833a-203">A partir do Windows Server 2003 com SP1, novos arquivos de log de erros podem ser criados com base na data e hora.</span><span class="sxs-lookup"><span data-stu-id="0833a-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="0833a-204">A substituição de hora e de data é controlada por dois novos valores de registro: **ErrorLoggingRolloverType** e **ErrorLoggingLocaltimeRollover**.</span><span class="sxs-lookup"><span data-stu-id="0833a-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="0833a-205">Para habilitar a substituição de data e hora, esses valores de registro devem ser adicionados ao registro.</span><span class="sxs-lookup"><span data-stu-id="0833a-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="0833a-206">O serviço http deve ser reiniciado quando essas chaves são adicionadas ao registro.</span><span class="sxs-lookup"><span data-stu-id="0833a-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="0833a-207">As chaves do registro de substituição do arquivo de log são criadas sob a seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="0833a-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="0833a-208">A chave do registro **ErrorLoggingRolloverType** indica o tipo de substituição desejado e é definida por padrão como a substituição baseada em tamanho.</span><span class="sxs-lookup"><span data-stu-id="0833a-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="0833a-209">A substituição também pode ser definida para ocorrer em uma base diária, semanal, mensal ou por hora.</span><span class="sxs-lookup"><span data-stu-id="0833a-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="0833a-210">Quando a substituição de arquivo é baseada no tempo, um valor de **ErrorLoggingLocaltimeRollover** de 0 indica que o tempo de substituição é expresso em GMT e um valor de 1 indica que o tempo de substituição é expresso na hora local.</span><span class="sxs-lookup"><span data-stu-id="0833a-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="0833a-211">A chave **ErrorLoggingRolloverType** pode usar um valor de 0 a 4, conforme listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0833a-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="0833a-212">Valor do tipo de substituição</span><span class="sxs-lookup"><span data-stu-id="0833a-212">Rollover type value</span></span> | <span data-ttu-id="0833a-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="0833a-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0833a-214">0</span><span class="sxs-lookup"><span data-stu-id="0833a-214">0</span></span>                   | <span data-ttu-id="0833a-215">Substituição baseada em tamanho.</span><span class="sxs-lookup"><span data-stu-id="0833a-215">Size based rollover.</span></span> <span data-ttu-id="0833a-216">Os arquivos de log são substituídos quando o arquivo atinge o tamanho definido na chave do registro **ErrorLogFileTruncateSize** .</span><span class="sxs-lookup"><span data-stu-id="0833a-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="0833a-217">1</span><span class="sxs-lookup"><span data-stu-id="0833a-217">1</span></span>                   | <span data-ttu-id="0833a-218">A substituição do arquivo de log ocorre diariamente.</span><span class="sxs-lookup"><span data-stu-id="0833a-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="0833a-219">2</span><span class="sxs-lookup"><span data-stu-id="0833a-219">2</span></span>                   | <span data-ttu-id="0833a-220">A substituição do arquivo de log ocorre semanalmente.</span><span class="sxs-lookup"><span data-stu-id="0833a-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="0833a-221">3</span><span class="sxs-lookup"><span data-stu-id="0833a-221">3</span></span>                   | <span data-ttu-id="0833a-222">A substituição do arquivo de log ocorre mensalmente.</span><span class="sxs-lookup"><span data-stu-id="0833a-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="0833a-223">4</span><span class="sxs-lookup"><span data-stu-id="0833a-223">4</span></span>                   | <span data-ttu-id="0833a-224">A substituição do arquivo de log ocorre por hora.</span><span class="sxs-lookup"><span data-stu-id="0833a-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="0833a-225">As convenções de nomenclatura para arquivos que armazenam os logs de erros são diferentes para o tamanho, a data e a substituição baseada em tempo.</span><span class="sxs-lookup"><span data-stu-id="0833a-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="0833a-226">A tabela a seguir lista as convenções de nomenclatura para arquivos de log http.</span><span class="sxs-lookup"><span data-stu-id="0833a-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="0833a-227">Tipo de Tollover</span><span class="sxs-lookup"><span data-stu-id="0833a-227">Tollover type</span></span> | <span data-ttu-id="0833a-228">Nome do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="0833a-228">Log file name</span></span>  | <span data-ttu-id="0833a-229">Descrição</span><span class="sxs-lookup"><span data-stu-id="0833a-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0833a-230">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0833a-230">Size</span></span>          | <span data-ttu-id="0833a-231">HTTPERRn. LOG</span><span class="sxs-lookup"><span data-stu-id="0833a-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="0833a-232">O arquivo de log é reciclado quando atinge um tamanho específico.</span><span class="sxs-lookup"><span data-stu-id="0833a-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="0833a-233">n é o número do arquivo e é incrementado quando o arquivo de log é substituído.</span><span class="sxs-lookup"><span data-stu-id="0833a-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="0833a-234">Diariamente</span><span class="sxs-lookup"><span data-stu-id="0833a-234">Daily</span></span>         | <span data-ttu-id="0833a-235">htYYMMDD. log</span><span class="sxs-lookup"><span data-stu-id="0833a-235">htYYMMDD.log</span></span>   | <span data-ttu-id="0833a-236">O arquivo de log é reciclado diariamente.</span><span class="sxs-lookup"><span data-stu-id="0833a-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="0833a-237">Semanalmente</span><span class="sxs-lookup"><span data-stu-id="0833a-237">Weekly</span></span>        | <span data-ttu-id="0833a-238">htYYMMww. log</span><span class="sxs-lookup"><span data-stu-id="0833a-238">htYYMMww.log</span></span>   | <span data-ttu-id="0833a-239">O arquivo de log é reciclado semanalmente, em que WW é a semana do mês.</span><span class="sxs-lookup"><span data-stu-id="0833a-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="0833a-240">Mensal</span><span class="sxs-lookup"><span data-stu-id="0833a-240">Monthly</span></span>       | <span data-ttu-id="0833a-241">htYYMM. log</span><span class="sxs-lookup"><span data-stu-id="0833a-241">htYYMM.log</span></span>     | <span data-ttu-id="0833a-242">O arquivo de log é reciclado a cada mês.</span><span class="sxs-lookup"><span data-stu-id="0833a-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="0833a-243">A cada hora</span><span class="sxs-lookup"><span data-stu-id="0833a-243">Hourly</span></span>        | <span data-ttu-id="0833a-244">htYYMMDDhh. log</span><span class="sxs-lookup"><span data-stu-id="0833a-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="0833a-245">O arquivo de log é reciclado por hora, em que HH é a hora do dia expressa em notação de 0-24 horas.</span><span class="sxs-lookup"><span data-stu-id="0833a-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




