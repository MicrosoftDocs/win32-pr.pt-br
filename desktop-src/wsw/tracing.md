---
title: Rastreamento
description: O rastreamento usa o ETW (rastreamento de eventos para Windows).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Rastreando serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366935"
---
# <a name="tracing"></a><span data-ttu-id="333b9-106">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="333b9-106">Tracing</span></span>

<span data-ttu-id="333b9-107">O rastreamento usa o ETW (rastreamento de eventos para Windows).</span><span class="sxs-lookup"><span data-stu-id="333b9-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="333b9-108">Para aproveitar as ferramentas de rastreamento disponíveis com o Windows Server 2008 R2, instale o SDK do Microsoft Windows no site de [downloads do MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .</span><span class="sxs-lookup"><span data-stu-id="333b9-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="333b9-109">Há três níveis de rastreamento com suporte:</span><span class="sxs-lookup"><span data-stu-id="333b9-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="333b9-110">Detalhado (todos os rastreamentos disponíveis).</span><span class="sxs-lookup"><span data-stu-id="333b9-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="333b9-111">Informações (rastreamentos informativos).</span><span class="sxs-lookup"><span data-stu-id="333b9-111">Info (informational traces).</span></span>
-   <span data-ttu-id="333b9-112">Erro (rastreamentos de erro).</span><span class="sxs-lookup"><span data-stu-id="333b9-112">Error (error traces).</span></span>

<span data-ttu-id="333b9-113">Os seguintes eventos são rastreados:</span><span class="sxs-lookup"><span data-stu-id="333b9-113">The following events are traced:</span></span>

-   <span data-ttu-id="333b9-114">Quaisquer erros (nível = erro, nível = informações ou nível = detalhado).</span><span class="sxs-lookup"><span data-stu-id="333b9-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="333b9-115">Entrada/saída de uma API (Level = info ou level = verbose).</span><span class="sxs-lookup"><span data-stu-id="333b9-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="333b9-116">Início e conclusão de qualquer e/s (Level = info ou level = verbose)</span><span class="sxs-lookup"><span data-stu-id="333b9-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="333b9-117">Mensagens SOAP trocadas (level = verbose, disponíveis no Windows 2003 SP1 e posterior)</span><span class="sxs-lookup"><span data-stu-id="333b9-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="333b9-118">Gerando e exibindo rastreamentos de WWSAPI</span><span class="sxs-lookup"><span data-stu-id="333b9-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="333b9-119">O WWSAPI usa os eventos baseados no manifesto no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="333b9-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="333b9-120">Como resultado, a experiência de rastreamento tem algumas diferenças com base na versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="333b9-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="333b9-121">A geração de rastreamentos de ETW pode ser feita usando as ferramentas de ETW in-box em todas as plataformas com suporte.</span><span class="sxs-lookup"><span data-stu-id="333b9-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="333b9-122">No entanto, a exibição dos rastreamentos ETW em um ótimo formato requer ferramentas personalizadas no Windows XP SP2 e no Windows 2003 SP1.</span><span class="sxs-lookup"><span data-stu-id="333b9-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="333b9-123">Há algumas maneiras diferentes de coletar e exibir rastreamentos de eventos do ETW WWSAPI dependendo da versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="333b9-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="333b9-124">Habilitando e exibindo rastreamentos do WWSAPI no Visualizador de Eventos (funciona no Windows Vista e superior)</span><span class="sxs-lookup"><span data-stu-id="333b9-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="333b9-125">Execute eventvwr. msc na linha de comando ou no menu executar.</span><span class="sxs-lookup"><span data-stu-id="333b9-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="333b9-126">Clique no link exibir no painel Ações à direita e habilite a opção Mostrar logs analíticos e de depuração.</span><span class="sxs-lookup"><span data-stu-id="333b9-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="333b9-127">Navegue até aplicativo e serviço logs \\ provedores do Microsoft \\ Windows \\ WebServices no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="333b9-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="333b9-128">Clique com o botão direito do mouse no provedor de rastreamento e selecione habilitar log.</span><span class="sxs-lookup"><span data-stu-id="333b9-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="333b9-129">Execute seu cenário.</span><span class="sxs-lookup"><span data-stu-id="333b9-129">Run your scenario.</span></span>
-   <span data-ttu-id="333b9-130">Ao atualizar a página do Visualizador de eventos, você deve começar a ver as entradas de rastreamento do WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="333b9-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="333b9-131">Habilitando e exibindo rastreamentos de WWSAPI usando o script Wstrace.bat (funciona no XPSP2 e acima)</span><span class="sxs-lookup"><span data-stu-id="333b9-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="333b9-132">O arquivo em lotes wstrace.bat fornece uma maneira conveniente para:</span><span class="sxs-lookup"><span data-stu-id="333b9-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="333b9-133">Criar um log de rastreamento</span><span class="sxs-lookup"><span data-stu-id="333b9-133">Create a trace log</span></span>
-   <span data-ttu-id="333b9-134">Excluir um log de rastreamento</span><span class="sxs-lookup"><span data-stu-id="333b9-134">Delete a trace log</span></span>
-   <span data-ttu-id="333b9-135">Habilitar e desabilitar o rastreamento</span><span class="sxs-lookup"><span data-stu-id="333b9-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="333b9-136">Atualizar o nível de rastreamento (info/Error/verbose)</span><span class="sxs-lookup"><span data-stu-id="333b9-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="333b9-137">Convertendo logs de rastreamento em arquivos CSV</span><span class="sxs-lookup"><span data-stu-id="333b9-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="333b9-138">O arquivo em lotes usa logman.exe para todos os comandos, com exceção da conversão dos logs para o arquivo CSV, que requer uma ferramenta personalizada (wstracedump.exe).</span><span class="sxs-lookup"><span data-stu-id="333b9-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="333b9-139">Usando comandos de rastreamento</span><span class="sxs-lookup"><span data-stu-id="333b9-139">Using tracing commands</span></span>

<span data-ttu-id="333b9-140">O comando a seguir cria um log que usa informações, o nível de erro ou detalhado.</span><span class="sxs-lookup"><span data-stu-id="333b9-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="333b9-141">Este comando requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="333b9-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="333b9-142">**wstrace.bat criar \[ erro de informações \| \| detalhadas\]**</span><span class="sxs-lookup"><span data-stu-id="333b9-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="333b9-143">O comando a seguir exclui o log.</span><span class="sxs-lookup"><span data-stu-id="333b9-143">The following command deletes the log.</span></span> <span data-ttu-id="333b9-144">Este comando requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="333b9-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="333b9-145">**wstrace.bat excluir**</span><span class="sxs-lookup"><span data-stu-id="333b9-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="333b9-146">O comando a seguir habilita o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="333b9-146">The following command enables tracing.</span></span> <span data-ttu-id="333b9-147">Primeiro, você deve criar um log.</span><span class="sxs-lookup"><span data-stu-id="333b9-147">You must first create a log.</span></span>

<span data-ttu-id="333b9-148">**wstrace.bat em**</span><span class="sxs-lookup"><span data-stu-id="333b9-148">**wstrace.bat on**</span></span>

<span data-ttu-id="333b9-149">O nível de rastreamento (info, Error ou verbose) pode ser modificado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="333b9-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="333b9-150">**\[ \| Erro detalhado de informações de atualização dewstrace.bat \|\]**</span><span class="sxs-lookup"><span data-stu-id="333b9-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="333b9-151">Para despejar a saída de rastreamento, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="333b9-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="333b9-152">**> de despejo dewstrace.bat temp.csv**</span><span class="sxs-lookup"><span data-stu-id="333b9-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="333b9-153">Os eventos serão despejados no arquivo CSV até que CTRL-C seja pressionado ou o rastreamento seja desabilitado.</span><span class="sxs-lookup"><span data-stu-id="333b9-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="333b9-154">Formato de arquivo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="333b9-154">Tracing File format</span></span>

<span data-ttu-id="333b9-155">Os arquivos CSV criados por wstrace.bat são arquivos de texto variáveis simples e separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="333b9-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="333b9-156">Esses arquivos podem ser abertos no Excel, no bloco de notas, etc.</span><span class="sxs-lookup"><span data-stu-id="333b9-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="333b9-157">As colunas do arquivo são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="333b9-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="333b9-158">TimeStamp-carimbo de data/hora de quando o evento foi registrado</span><span class="sxs-lookup"><span data-stu-id="333b9-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="333b9-159">ProcessID-ID ULONG do processo que registra o evento</span><span class="sxs-lookup"><span data-stu-id="333b9-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="333b9-160">ID ThreadID-ULONG do thread que está registrando o evento</span><span class="sxs-lookup"><span data-stu-id="333b9-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="333b9-161">O valor enumerado de evento do tipo de evento pode ser ("API Enter" "API \| pendente" "API \| ExitSyncSuccess" \| "API ExitSyncFailure" \| "API ExitAsyncSuccess" \| "API ExitAsyncFailure" " \| e/s iniciada" \| "e/s concluído" \| "falha de e/s" " \| erro" \| "mensagem recebida iniciada" "mensagem recebida" "mensagem recebida \| \| parada" \| "enviando mensagem iniciada" \| "enviando mensagem" \| "enviando mensagem parada")</span><span class="sxs-lookup"><span data-stu-id="333b9-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="333b9-162">Operation-o nome da operação que está sendo invocada.</span><span class="sxs-lookup"><span data-stu-id="333b9-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="333b9-163">Normalmente, isso é mapeado para a API que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="333b9-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="333b9-164">Erro-número de erro HRESULT opcional</span><span class="sxs-lookup"><span data-stu-id="333b9-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="333b9-165">Informações-informações opcionais sobre o evento</span><span class="sxs-lookup"><span data-stu-id="333b9-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="333b9-166">Coletando arquivo de rastreamento ETW WWSAPI usando ferramentas de ETW (funciona no XPSP2 e superior)</span><span class="sxs-lookup"><span data-stu-id="333b9-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="333b9-167">Habilitando o rastreamento ETW para WWSAPI</span><span class="sxs-lookup"><span data-stu-id="333b9-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="333b9-168">**logman start wstrace-BS 64-pés 1-RT-p Microsoft-Windows-WebServices \[ flags \[ nível \] \] \[ -o <EtlLogFileName> \] -ETS**</span><span class="sxs-lookup"><span data-stu-id="333b9-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="333b9-169">para criar e iniciar a sessão de rastreamento ETW.</span><span class="sxs-lookup"><span data-stu-id="333b9-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="333b9-170">Logman.exe é uma ferramenta de ETW na caixa disponível em todas as plataformas com suporte.</span><span class="sxs-lookup"><span data-stu-id="333b9-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="333b9-171">Observe que você precisa usar o Microsoft \_ Windows \_ WebServices como o nome do provedor no xpsp2 e no W2K3.</span><span class="sxs-lookup"><span data-stu-id="333b9-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="333b9-172">Você pode executar provedores de consulta logman para ver a lista de provedores registrados.</span><span class="sxs-lookup"><span data-stu-id="333b9-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="333b9-173">O provedor Microsoft-Windows-WebServices (ou Microsoft \_ Windows \_ WebServices) deve ser listado, a menos que não esteja registrado.</span><span class="sxs-lookup"><span data-stu-id="333b9-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="333b9-174">O provedor normalmente é registrado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="333b9-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="333b9-175">No entanto, ele também pode ser registrado manualmente executando wevtutil.exe mensagem instantânea <ManifestFileName> (no Windows Vista e posterior) ou mofcomp.exe <MofFileName> (no xpsp2 e no W2K3).</span><span class="sxs-lookup"><span data-stu-id="333b9-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="333b9-176">Os sinalizadores podem ser usados para filtrar os rastreamentos por seu tipo.</span><span class="sxs-lookup"><span data-stu-id="333b9-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="333b9-177">Pode ser ou um valor para os seguintes tipos de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="333b9-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="333b9-178">Se não for fornecido, todos os tipos de rastreamento serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="333b9-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="333b9-179">0x1-rastreamentos de entrada/saída da API.</span><span class="sxs-lookup"><span data-stu-id="333b9-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="333b9-180">0x2-rastreamentos de erro.</span><span class="sxs-lookup"><span data-stu-id="333b9-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="333b9-181">0x4-rastreamentos de e/s.</span><span class="sxs-lookup"><span data-stu-id="333b9-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="333b9-182">os rastreamentos de mensagens 0x8-SOAP.</span><span class="sxs-lookup"><span data-stu-id="333b9-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="333b9-183">0x10-rastreamentos de mensagens binários.</span><span class="sxs-lookup"><span data-stu-id="333b9-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="333b9-184">O nível pode ser usado para filtrar os rastreamentos por seu nível.</span><span class="sxs-lookup"><span data-stu-id="333b9-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="333b9-185">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="333b9-185">It should be one of the following values.</span></span> <span data-ttu-id="333b9-186">Se não for fornecido, todos os níveis de rastreamento serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="333b9-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="333b9-187">0x1-rastreamentos fatais.</span><span class="sxs-lookup"><span data-stu-id="333b9-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="333b9-188">0x2-rastreamentos de erro.</span><span class="sxs-lookup"><span data-stu-id="333b9-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="333b9-189">0x3-rastreamentos de aviso.</span><span class="sxs-lookup"><span data-stu-id="333b9-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="333b9-190">0x4-rastreamentos informativos.</span><span class="sxs-lookup"><span data-stu-id="333b9-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="333b9-191">0x5-rastreamentos detalhados.</span><span class="sxs-lookup"><span data-stu-id="333b9-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="333b9-192">EtlLogFileName é o caminho para o arquivo de log de eventos do ETW a ser criado (use a extensão. ETL).</span><span class="sxs-lookup"><span data-stu-id="333b9-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="333b9-193">Se não for fornecido, o ETW escolherá um nome aleatório que poderá ser consultado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="333b9-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="333b9-194">Esse arquivo não deve residir no diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="333b9-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="333b9-195">O arquivo de log de eventos do ETW (arquivo. ETL) está em formato binário.</span><span class="sxs-lookup"><span data-stu-id="333b9-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="333b9-196">Ele pode ser consumido por aplicativos ETW, mas não está no formato legível humana.</span><span class="sxs-lookup"><span data-stu-id="333b9-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="333b9-197">A próxima etapa descreve como exibir seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="333b9-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="333b9-198">Execute seu cenário</span><span class="sxs-lookup"><span data-stu-id="333b9-198">Run your scenario</span></span>

<span data-ttu-id="333b9-199">Coletando arquivo de log de eventos ETW.</span><span class="sxs-lookup"><span data-stu-id="333b9-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="333b9-200">**logman Stop wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="333b9-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="333b9-201">para interromper a sessão de rastreamento ETW.</span><span class="sxs-lookup"><span data-stu-id="333b9-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="333b9-202">Isso ocorre quando o ETW para de registrar os eventos.</span><span class="sxs-lookup"><span data-stu-id="333b9-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="333b9-203">O arquivo de log de eventos do ETW (especificado no parâmetro EtlLogFileName) está pronto para consumir.</span><span class="sxs-lookup"><span data-stu-id="333b9-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="333b9-204">Ele pode ser exibido localmente (instruções são fornecidas abaixo) ou enviado ao grupo de produtos para investigação.</span><span class="sxs-lookup"><span data-stu-id="333b9-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="333b9-205">Exemplo de ponta a ponta usando ferramentas de ETW:</span><span class="sxs-lookup"><span data-stu-id="333b9-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="333b9-206">**logman start wstrace-BS 64-FT 1-RT-p Microsoft-Windows-WebServices-o mytrace. etl-ETS**</span><span class="sxs-lookup"><span data-stu-id="333b9-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="333b9-207">**Echo.. Execute seu cenário..**</span><span class="sxs-lookup"><span data-stu-id="333b9-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="333b9-208">**logman Stop wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="333b9-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="333b9-209">**Tracerpt mytrace. etl-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="333b9-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="333b9-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="333b9-210">**wstrace.htm**</span></span>

<span data-ttu-id="333b9-211">**Echo.. Use mytrace.xml e wstrace. xsl na página aberta.**</span><span class="sxs-lookup"><span data-stu-id="333b9-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="333b9-212">Exibindo rastreamentos de arquivos de rastreamento ETW WWSAPI usando a ferramenta wstracedump.exe (funciona no Windows XP e versões posteriores)</span><span class="sxs-lookup"><span data-stu-id="333b9-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="333b9-213">Wstracedump.exe é uma ferramenta de consumidor ETW personalizada desenvolvida que processa eventos no arquivo de rastreamento ETW WWSAPI e produz saída legível humana.</span><span class="sxs-lookup"><span data-stu-id="333b9-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="333b9-214">Ele pode produzir a saída de todas as plataformas com suporte.</span><span class="sxs-lookup"><span data-stu-id="333b9-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="333b9-215">Veja seu uso (wstracedump.exe-?) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="333b9-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="333b9-216">Exibindo rastreamentos de arquivos de rastreamento ETW WWSAPI usando as ferramentas de ETW (funciona no Windows Vista e versões posteriores)</span><span class="sxs-lookup"><span data-stu-id="333b9-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="333b9-217">Tracerpt.exe é a ferramenta para exibir o conteúdo de um arquivo de log de eventos ETW e disponível em todas as plataformas com suporte.</span><span class="sxs-lookup"><span data-stu-id="333b9-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="333b9-218">Ele pode ser usado para gerar arquivos de despejo CSV, EVTX ou XML de um arquivo de log de eventos do ETW.</span><span class="sxs-lookup"><span data-stu-id="333b9-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="333b9-219">No entanto, o arquivo de saída gerado tem rastreamentos legíveis somente no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="333b9-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="333b9-220">Estas instruções descrevem como gerar o arquivo de despejo XML e usá-lo junto com um arquivo XSL para exibir os rastreamentos em um bom formato (o arquivo XSL é muito trivial e pode ser alterado se forem desejados formatos diferentes).</span><span class="sxs-lookup"><span data-stu-id="333b9-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="333b9-221">Executar</span><span class="sxs-lookup"><span data-stu-id="333b9-221">Run</span></span>

    <span data-ttu-id="333b9-222">**Tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="333b9-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="333b9-223">para criar um despejo XML a partir do arquivo ETL binário (tracerpt.exe cria o arquivo de saída em formato XML por padrão.</span><span class="sxs-lookup"><span data-stu-id="333b9-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="333b9-224">Executar Tracerpt-?</span><span class="sxs-lookup"><span data-stu-id="333b9-224">Run tracerpt -?</span></span> <span data-ttu-id="333b9-225">Para ver outros formatos disponíveis).</span><span class="sxs-lookup"><span data-stu-id="333b9-225">To see other available formats).</span></span>

-   <span data-ttu-id="333b9-226">Neste ponto, você pode ver as informações de rastreamento no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="333b9-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="333b9-227">Além disso, você pode abrir o arquivo de wstrace.htm e usar o arquivo de despejo XML e o arquivo wstrace. xsl para ver os rastreamentos em um formato mais interessante.</span><span class="sxs-lookup"><span data-stu-id="333b9-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="333b9-228">Observe que os arquivos precisam estar no computador local para poderem usar esse arquivo HTML no IE.</span><span class="sxs-lookup"><span data-stu-id="333b9-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="333b9-229">Segurança</span><span class="sxs-lookup"><span data-stu-id="333b9-229">Security</span></span>

<span data-ttu-id="333b9-230">Ao habilitar o rastreamento, os administradores devem levar em conta que consome espaço em disco e capacidade de computação adicionais.</span><span class="sxs-lookup"><span data-stu-id="333b9-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="333b9-231">Um cliente mal-intencionado ou aplicativo pode esgotar os recursos do sistema, a menos que as configurações de rastreamento sejam definidas com limites razoáveis.</span><span class="sxs-lookup"><span data-stu-id="333b9-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="333b9-232">Ao usar o recurso de rastreamento de mensagens, as mensagens que realizam informações confidenciais, como credenciais, informações pessoais etc., podem ser mantidas no disco ou exibidas por qualquer pessoa que tenha acesso ao Visualizador de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="333b9-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="333b9-233">Como uma mitigação desse problema, o rastreamento pode ser habilitado por usuários do sistema ou administrador no Windows 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="333b9-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="333b9-234">O rastreamento de mensagens é desabilitado no Windows XP no qual qualquer usuário pode ativar o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="333b9-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="333b9-235">A seguinte enumeração é usada com o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="333b9-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="333b9-236">**\_API de rastreamento do WS \_**</span><span class="sxs-lookup"><span data-stu-id="333b9-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




