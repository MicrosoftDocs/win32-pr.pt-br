---
description: A ferramenta de configuração de rastreamento do Microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, é usada para configurar recursos de rastreamento para fins de depuração e detecção de pacotes.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, uma ferramenta de configuração de rastreamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793357"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="12961-103">WinHttpTraceCfg.exe, uma ferramenta de configuração de rastreamento</span><span class="sxs-lookup"><span data-stu-id="12961-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="12961-104">A ferramenta de configuração de rastreamento do [Microsoft Windows http Services (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, é usada para configurar recursos de rastreamento para fins de depuração e detecção de pacotes.</span><span class="sxs-lookup"><span data-stu-id="12961-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="12961-105">A capacidade de monitorar as funções WinHTTP e seu tráfego de rede correspondente é importante.</span><span class="sxs-lookup"><span data-stu-id="12961-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="12961-106">Depurar aplicativos que utilizam protocolos de transmissão criptografada, como protocolo SSL (SSL), impedir a detecção de pacotes na camada de transporte de rede e exigir a capacidade de interceptar o tráfego entre o cliente e o servidor depois que ele tiver sido descriptografado.</span><span class="sxs-lookup"><span data-stu-id="12961-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="12961-107">O Microsoft Windows HTTP Services (WinHTTP) fornece um recurso de rastreamento que tem uma variedade de recursos para interceptar o fluxo de tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="12961-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="12961-108">Esse recurso de rastreamento pode ser uma ferramenta valiosa para depuração.</span><span class="sxs-lookup"><span data-stu-id="12961-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="12961-109">Ele pode ser usado, por exemplo, para exibir parâmetros passados para várias chamadas de função, bem como para exibir dados reais enviados e recebidos por um aplicativo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="12961-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="12961-110">Usando o recurso de rastreamento</span><span class="sxs-lookup"><span data-stu-id="12961-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="12961-111">Interpretando dados de rastreamento</span><span class="sxs-lookup"><span data-stu-id="12961-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="12961-112">Usando o recurso de rastreamento</span><span class="sxs-lookup"><span data-stu-id="12961-112">Using the Trace Facility</span></span>

<span data-ttu-id="12961-113">O WinHTTP Obtém os parâmetros de controle de rastreamento do registro.</span><span class="sxs-lookup"><span data-stu-id="12961-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="12961-114">Esses parâmetros de controle afetam como o WinHTTP produz a saída de rastreamento e como essa saída é formatada.</span><span class="sxs-lookup"><span data-stu-id="12961-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="12961-115">Todos os aplicativos que usam WinHTTP compartilham as mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="12961-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="12961-116">Uma ferramenta de configuração de recurso de rastreamento, WinHttpTraceCfg.exe, está disponível como um download no site de [Ferramentas do Windows Server 2003 Resource Kit](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="12961-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="12961-117">A ferramenta de configuração define ou recupera as configurações do registro de recurso de rastreamento com base nos parâmetros de linha de comando especificados.</span><span class="sxs-lookup"><span data-stu-id="12961-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="12961-118">A tabela a seguir lista os possíveis parâmetros para a ferramenta de configuração do.</span><span class="sxs-lookup"><span data-stu-id="12961-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12961-119">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="12961-119">Parameter</span></span></th>
<th><span data-ttu-id="12961-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="12961-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12961-121">-?</span><span class="sxs-lookup"><span data-stu-id="12961-121">-?</span></span></td>
<td><span data-ttu-id="12961-122">Exibe dados de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="12961-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-123">-E</span><span class="sxs-lookup"><span data-stu-id="12961-123">-e</span></span></td>
<td><span data-ttu-id="12961-124">Especifica se o recurso de rastreamento está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="12961-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12961-125">0</span><span class="sxs-lookup"><span data-stu-id="12961-125">0</span></span></td>
<td><span data-ttu-id="12961-126">Configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="12961-126">Default setting.</span></span> <span data-ttu-id="12961-127">Desabilita o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-128">1</span><span class="sxs-lookup"><span data-stu-id="12961-128">1</span></span></td>
<td><span data-ttu-id="12961-129">Habilita o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12961-130">-l</span><span class="sxs-lookup"><span data-stu-id="12961-130">-l</span></span></td>
<td><p><span data-ttu-id="12961-131">Especifica um prefixo para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="12961-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="12961-132">O prefixo pode incluir um caminho.</span><span class="sxs-lookup"><span data-stu-id="12961-132">The prefix can include a path.</span></span> <span data-ttu-id="12961-133">O arquivo de log é gravado no diretório atual ou no diretório especificado no prefixo e tem o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="12961-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="12961-134"><<em></em> > prefixo -< <em>nome do aplicativo</em> > . <em>Tempo</em>de <> . log</span><span class="sxs-lookup"><span data-stu-id="12961-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="12961-135">Se um prefixo não for especificado, uma cadeia de caracteres vazia será usada.</span><span class="sxs-lookup"><span data-stu-id="12961-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="12961-136">Especifique &quot; \* &quot; para excluir um prefixo existente.</span><span class="sxs-lookup"><span data-stu-id="12961-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-137">-d</span><span class="sxs-lookup"><span data-stu-id="12961-137">-d</span></span></td>
<td><p><span data-ttu-id="12961-138">Especifica se a saída do rastreamento é exibida em um depurador ou gravada em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="12961-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12961-139">0</span><span class="sxs-lookup"><span data-stu-id="12961-139">0</span></span></td>
<td><span data-ttu-id="12961-140">Configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="12961-140">Default setting.</span></span> <span data-ttu-id="12961-141">Grava no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="12961-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-142">1</span><span class="sxs-lookup"><span data-stu-id="12961-142">1</span></span></td>
<td><span data-ttu-id="12961-143">Exibe em um depurador.</span><span class="sxs-lookup"><span data-stu-id="12961-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12961-144">-S</span><span class="sxs-lookup"><span data-stu-id="12961-144">-s</span></span></td>
<td><p><span data-ttu-id="12961-145">Especifica como o tráfego de rede (solicitações e respostas) é exibido.</span><span class="sxs-lookup"><span data-stu-id="12961-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12961-146">0</span><span class="sxs-lookup"><span data-stu-id="12961-146">0</span></span></td>
<td><span data-ttu-id="12961-147">Exibe somente cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="12961-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-148">1</span><span class="sxs-lookup"><span data-stu-id="12961-148">1</span></span></td>
<td><span data-ttu-id="12961-149">Configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="12961-149">Default setting.</span></span> <span data-ttu-id="12961-150">Mostra o tráfego de rede no formato American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="12961-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12961-151">2</span><span class="sxs-lookup"><span data-stu-id="12961-151">2</span></span></td>
<td><span data-ttu-id="12961-152">Mostra o tráfego de rede no formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="12961-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-153">-T</span><span class="sxs-lookup"><span data-stu-id="12961-153">-t</span></span></td>
<td><p><span data-ttu-id="12961-154">Especifica se as chamadas de função de nível superior são registradas no rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12961-155">0</span><span class="sxs-lookup"><span data-stu-id="12961-155">0</span></span></td>
<td><span data-ttu-id="12961-156">Configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="12961-156">Default setting.</span></span> <span data-ttu-id="12961-157">As chamadas de função não são registradas.</span><span class="sxs-lookup"><span data-stu-id="12961-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12961-158">1</span><span class="sxs-lookup"><span data-stu-id="12961-158">1</span></span></td>
<td><span data-ttu-id="12961-159">As chamadas de função de nível superior são registradas.</span><span class="sxs-lookup"><span data-stu-id="12961-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12961-160">-M</span><span class="sxs-lookup"><span data-stu-id="12961-160">-m</span></span></td>
<td><p><span data-ttu-id="12961-161">Especifica o tamanho máximo, em bytes, de um arquivo de log gerado pelo recurso de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="12961-162">Se essa opção for especificada sem um tamanho, o valor mínimo será 65.535 bytes.</span><span class="sxs-lookup"><span data-stu-id="12961-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="12961-163">Se um arquivo de log atingir o tamanho máximo, o conteúdo do arquivo será apagado.</span><span class="sxs-lookup"><span data-stu-id="12961-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="12961-164">Os dados de rastreamento continuam a ser gravados no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="12961-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="12961-165">A execução da ferramenta de configuração de recurso de rastreamento e a especificação de nenhum parâmetro recupera e exibe as configurações atuais do registro.</span><span class="sxs-lookup"><span data-stu-id="12961-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="12961-166">Os arquivos de log crescem rapidamente e prejudicam o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="12961-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="12961-167">Verifique se o espaço necessário na unidade de disco rígido está disponível antes de habilitar o recurso de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="12961-168">Interpretando dados de rastreamento</span><span class="sxs-lookup"><span data-stu-id="12961-168">Interpreting Trace Data</span></span>

<span data-ttu-id="12961-169">O fluxo de dados de recursos de rastreamento reflete as funções de WinHTTP chamadas no aplicativo e todos os dados HTTP enviados ou recebidos.</span><span class="sxs-lookup"><span data-stu-id="12961-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="12961-170">Em alguns casos, as funções chamadas internamente pelo WinHTTP também são mostradas.</span><span class="sxs-lookup"><span data-stu-id="12961-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="12961-171">A imagem a seguir mostra uma parte de um arquivo de log gerado pelo recurso de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="12961-172">Vários itens são realçados e rotulados.</span><span class="sxs-lookup"><span data-stu-id="12961-172">Several items are highlighted and labeled.</span></span>

![rastreamento de exemplo](images/ss-tracer-wco.png)

<span data-ttu-id="12961-174">Cada linha da saída de rastreamento contém informações em três colunas.</span><span class="sxs-lookup"><span data-stu-id="12961-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="12961-175">A primeira coluna mostra a data e a hora em que a entrada foi registrada.</span><span class="sxs-lookup"><span data-stu-id="12961-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="12961-176">A segunda coluna mostra um identificador de solicitação (ID) que pode ser usado para diferenciar entre várias solicitações.</span><span class="sxs-lookup"><span data-stu-id="12961-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="12961-177">Se a entrada de log não corresponder a uma solicitação específica, " \* sessão \* " será exibida nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="12961-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="12961-178">Pode ser útil classificar o arquivo de log com base nessa ID para ver apenas os eventos que ocorrem para uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="12961-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="12961-179">O exemplo a seguir mostra um comando que você pode usar para classificar o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="12961-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="12961-180">**findstr 00000001 LogFile. log**</span><span class="sxs-lookup"><span data-stu-id="12961-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="12961-181">A terceira coluna mostra uma chamada de função, um tráfego HTTP ou uma mensagem de status incluída para ajudar a interpretar o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="12961-182">Quando uma entrada de log corresponde a uma chamada de função, os parâmetros da função também são registrados.</span><span class="sxs-lookup"><span data-stu-id="12961-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="12961-183">Os endereços de memória são exibidos em hexadecimal, enquanto todos os outros valores são exibidos como uma cadeia de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="12961-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="12961-184">O recurso de rastreamento também registra a hora de retorno e o valor de cada função.</span><span class="sxs-lookup"><span data-stu-id="12961-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="12961-185">O formato dos dados HTTP depende das configurações do registro especificadas com a ferramenta de configuração do recurso de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="12961-186">Quando os dados HTTP são criptografados, os dados descriptografados também são mostrados na saída do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="12961-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




