---
description: .
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Controle do rastreamento do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b15ece4581525fddc25213c630e24d0e49110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773097"
---
# <a name="control-of-winsock-tracing"></a><span data-ttu-id="e4e7c-103">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-103">Control of Winsock Tracing</span></span>

<span data-ttu-id="e4e7c-104">O rastreamento do Winsock pode ser controlado usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-104">Winsock tracing can be controlled by using either of the following methods:</span></span>

-   <span data-ttu-id="e4e7c-105">Ferramentas da linha de comando</span><span class="sxs-lookup"><span data-stu-id="e4e7c-105">Command-line tools</span></span>

    <span data-ttu-id="e4e7c-106">Duas ferramentas de linha de comando estão incluídas no Windows Vista e no Windows Server 2008 que são usadas para controlar o rastreamento e converter o arquivo de log de rastreamento binário em texto legível.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-106">Two command-line tools are included with Windows Vista and Windows Server 2008 that are used to control tracing and convert the binary trace log file to readable text.</span></span>

    <span data-ttu-id="e4e7c-107">A ferramenta **logman.exe** é usada para iniciar ou parar o rastreamento do Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-107">The **logman.exe** tool is used to start or stop Winsock tracing.</span></span>

    <span data-ttu-id="e4e7c-108">A ferramenta de **tracerpt.exe** é usada para converter o arquivo de log de rastreamento binário em um arquivo de texto legível.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-108">The **tracerpt.exe** tool is used to convert the binary trace log file to a readable text file.</span></span>

-   <span data-ttu-id="e4e7c-109">Visualizador de Eventos</span><span class="sxs-lookup"><span data-stu-id="e4e7c-109">Event Viewer</span></span>

    <span data-ttu-id="e4e7c-110">O Visualizador de Eventos no Windows Vista e posterior também pode ser usado para habilitar o rastreamento do Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-110">The Event Viewer on Windows Vista and later can also be used to enable Winsock tracing.</span></span> <span data-ttu-id="e4e7c-111">O Visualizador de Eventos é acessível nas ferramentas administrativas do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-111">The Event Viewer is accessible under the Administrative Tools from the Start menu.</span></span>

## <a name="using-logman-and-tracert"></a><span data-ttu-id="e4e7c-112">Usando Logman e tracert</span><span class="sxs-lookup"><span data-stu-id="e4e7c-112">Using logman and tracert</span></span>

<span data-ttu-id="e4e7c-113">O rastreamento de eventos de rede do Winsock é desabilitado por padrão no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-113">Winsock network event tracing is disabled by default on Windows Vista and later.</span></span>

<span data-ttu-id="e4e7c-114">O comando a seguir inicia o rastreamento de eventos de rede do Winsock em um computador, define o nome da sessão de rastreamento de eventos como mywinsocksession e envia a saída para um arquivo de log binário chamado winsocklogfile. etl:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-114">The following command starts Winsock network event tracing on a computer, sets the name of event trace session to mywinsocksession, and sends output to a binary log file called winsocklogfile.etl:</span></span>

<span data-ttu-id="e4e7c-115">**logman start-ETS mywinsocksession-o winsocklogfile. etl-p Microsoft-Windows-Winsock-AFD**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-115">**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**</span></span>

<span data-ttu-id="e4e7c-116">Os arquivos de log são criados no diretório atual com nomes de arquivo do formato winsocklogfile \_ 000001. etl</span><span class="sxs-lookup"><span data-stu-id="e4e7c-116">Log files are created in the current directory with filenames of the form winsocklogfile\_000001.etl</span></span>

<span data-ttu-id="e4e7c-117">O comando a seguir interrompe o rastreamento do Winsock acima em um computador para a sessão chamada mywinsocksession:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-117">The following command stops the above Winsock tracing on a computer for the session named mywinsocksession:</span></span>

<span data-ttu-id="e4e7c-118">**logman Stop-ETS mywinsocksession**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-118">**logman stop -ets mywinsocksession**</span></span>

<span data-ttu-id="e4e7c-119">Um arquivo de log binário será gravado no local especificado pelo parâmetro – o.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-119">A binary log file will be written to the location specified by the –o parameter.</span></span> <span data-ttu-id="e4e7c-120">Para converter o arquivo binário em um arquivo de texto legível, **tracerpt.exe** é usado:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-120">To translate the binary file into a readable text file, **tracerpt.exe** is used:</span></span>

<span data-ttu-id="e4e7c-121">**tracerpt.exe <nome do arquivo. etl> – o winsocktracelog.txt**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-121">**tracerpt.exe <name of the .etl file> –o winsocktracelog.txt**</span></span>

<span data-ttu-id="e4e7c-122">Se um arquivo de saída contendo XML em vez de texto sem formatação for preferencial, o seguinte comando será usado:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-122">If an output file containing xml rather than plain text is preferred, the following command is used:</span></span>

<span data-ttu-id="e4e7c-123">**tracerpt.exe <nome do arquivo. etl> – o winsocktracelog.xml – do XML**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-123">**tracerpt.exe <name of the .etl file> –o winsocktracelog.xml –of xml**</span></span>

<span data-ttu-id="e4e7c-124">O rastreamento de alterações do catálogo Winsock é habilitado por padrão no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-124">Winsock catalog change tracing is enabled by default on Windows Vista and later.</span></span>

> [!Note]  
> <span data-ttu-id="e4e7c-125">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-125">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="e4e7c-126">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="e4e7c-126">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="e4e7c-127">O comando a seguir inicia o rastreamento de alterações do catálogo Winsock para provedores de serviço em camadas (LSPs) em um computador, define o nome da sessão de rastreamento de eventos como mywinsockcatalogsession e envia a saída para um arquivo de log binário chamado winsockcataloglogfile. etl:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-127">The following command starts Winsock Catalog Change tracing for layered service providers (LSPs) on a computer, sets the name of event trace session to mywinsockcatalogsession, and sends output to a binary log file called winsockcataloglogfile.etl:</span></span>

<span data-ttu-id="e4e7c-128">**logman start-ETS mywinsockcatalogsession-o winsockcataloglogfile. etl-p Microsoft-Windows-Winsock-WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-128">**logman start -ets mywinsockcatalogsession -o winsockcataloglogfile.etl -p Microsoft-Windows-Winsock-WS2HELP**</span></span>

<span data-ttu-id="e4e7c-129">Os arquivos de log são criados no diretório atual com nomes de arquivo do formato winsockcataloglogfile \_ 000001. etl</span><span class="sxs-lookup"><span data-stu-id="e4e7c-129">Log files are created in the current directory with filenames of the form winsockcataloglogfile\_000001.etl</span></span>

<span data-ttu-id="e4e7c-130">O comando a seguir interrompe o rastreamento do Winsock acima em um computador para a sessão chamada MySession:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-130">The following command stops the above Winsock tracing on a computer for the session named mysession:</span></span>

<span data-ttu-id="e4e7c-131">**logman Stop-ETS mywinsockcatalogsession**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-131">**logman stop -ets mywinsockcatalogsession**</span></span>

<span data-ttu-id="e4e7c-132">Um arquivo de log binário será gravado no local especificado pelo parâmetro – o.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-132">A binary log file will be written to the location specified by the –o parameter.</span></span> <span data-ttu-id="e4e7c-133">Para converter o arquivo binário em um arquivo de texto legível, **tracerpt.exe** é usado:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-133">To translate the binary file into a readable text file, **tracerpt.exe** is used:</span></span>

<span data-ttu-id="e4e7c-134">**tracerpt.exe <nome do arquivo. etl> – o winsockcatalogtracelog.txt**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-134">**tracerpt.exe <name of the .etl file> –o winsockcatalogtracelog.txt**</span></span>

<span data-ttu-id="e4e7c-135">Se um arquivo de saída contendo XML em vez de texto sem formatação for preferencial, o seguinte comando será usado:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-135">If an output file containing xml rather than plain text is preferred, the following command is used:</span></span>

<span data-ttu-id="e4e7c-136">**tracerpt.exe <nome do arquivo. etl> – o winsockcatalogtracelog.xml – do XML**</span><span class="sxs-lookup"><span data-stu-id="e4e7c-136">**tracerpt.exe <name of the .etl file> –o winsockcatalogtracelog.xml –of xml**</span></span>

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a><span data-ttu-id="e4e7c-137">Usando Visualizador de Eventos para iniciar o rastreamento de eventos de rede do Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-137">Using Event Viewer to Start Winsock Network Event Tracing</span></span>

<span data-ttu-id="e4e7c-138">Quando você abre Visualizador de Eventos, o painel esquerdo contém a lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-138">When you open Event Viewer, the left pane contains the list of events.</span></span> <span data-ttu-id="e4e7c-139">Abra **logs de aplicativos e serviços** e navegue até o **evento de \\ \\ rede Winsock do Microsoft Windows** como a origem e selecione **operacional**.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-139">Open **Applications and Services Logs** and navigate to **Microsoft\\Windows\\Winsock Network Event** as the source and select **Operational**.</span></span>

<span data-ttu-id="e4e7c-140">No painel Ação, selecione **Propriedades do log** e marque a caixa de seleção **habilitar registro em log** .</span><span class="sxs-lookup"><span data-stu-id="e4e7c-140">In the Action pane, select **Log Properties** and check the **Enable Logging** check box.</span></span> <span data-ttu-id="e4e7c-141">Quando o registro em log estiver habilitado, você também poderá alterar o tamanho do arquivo de log se isso for necessário.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-141">Once logging is enabled, you can also change the size of the log file if this is needed.</span></span>

<span data-ttu-id="e4e7c-142">O rastreamento de eventos de rede do Winsock agora está habilitado e tudo o que você precisa fazer é pressionar a ação atualizar para atualizar a lista de eventos que foram registrados.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-142">Winsock network event tracing is now enabled and all you need to do is hit the Refresh action to update the list of events that have been logged.</span></span> <span data-ttu-id="e4e7c-143">Para interromper o registro em log, basta desmarcar o mesmo botão de opção.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-143">To stop logging, simply uncheck the same radio button.</span></span>

<span data-ttu-id="e4e7c-144">Talvez seja necessário aumentar o tamanho do log dependendo de quantos eventos você deseja ver.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-144">You may need to increase the log size depending on how many events you want to see.</span></span> <span data-ttu-id="e4e7c-145">Uma desvantagem de usar o Visualizador de Eventos para o rastreamento de Winsock é que ele não carrega todos os recursos de cadeia de caracteres, de modo que as mensagens exibidas no campo Descrição (depois que você seleciona um evento) às vezes são difíceis de serem lidas (um argumento que deve ser formatado como hex será exibido em decimal, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="e4e7c-145">One drawback to using the Event Viewer for Winsock tracing is that it does not load all the string resources so the messages displayed in the Description field (once you select an event) is sometimes hard to read (an argument that should be formatted as hex will be displayed in decimal, for example).</span></span> <span data-ttu-id="e4e7c-146">No entanto, você pode selecionar a guia **detalhes** na descrição do evento que mostra a entrada de log XML bruto que geralmente tem mais facilidade para entender os argumentos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-146">However, you can select the **Details** tab in the event description which shows the raw XML log entry which usually has easier to understand arguments.</span></span>

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a><span data-ttu-id="e4e7c-147">Usando Visualizador de Eventos para iniciar o rastreamento de alterações do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-147">Using Event Viewer to Start Winsock Catalog Change Tracing</span></span>

<span data-ttu-id="e4e7c-148">Quando você abre Visualizador de Eventos, o painel esquerdo contém a lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-148">When you open Event Viewer, the left pane contains the list of events.</span></span> <span data-ttu-id="e4e7c-149">Abra **logs de aplicativos e serviços** e navegue até a **alteração do catálogo do \\ \\ Winsock do Microsoft Windows** como a origem e selecione **operacional**.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-149">Open **Applications and Services Logs** and navigate to **Microsoft\\Windows\\Winsock Catalog Change** as the source and select **Operational**.</span></span>

<span data-ttu-id="e4e7c-150">No painel Ação, selecione **Propriedades do log** e marque a caixa de seleção **habilitar registro em log** .</span><span class="sxs-lookup"><span data-stu-id="e4e7c-150">In the Action pane, select **Log Properties** and check the **Enable Logging** check box.</span></span> <span data-ttu-id="e4e7c-151">Quando o registro em log estiver habilitado, você também poderá alterar o tamanho do arquivo de log se isso for necessário.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-151">Once logging is enabled, you can also change the size of the log file if this is needed.</span></span>

<span data-ttu-id="e4e7c-152">O rastreamento de alterações do catálogo do Winsock agora está habilitado e tudo o que você precisa fazer é pressionar a ação atualizar para atualizar a lista de eventos que foram registrados.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-152">Winsock catalog change tracing is now enabled and all you need to do is hit the Refresh action to update the list of events that have been logged.</span></span> <span data-ttu-id="e4e7c-153">Para interromper o registro em log, basta desmarcar o mesmo botão de opção.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-153">To stop logging, simply uncheck the same radio button.</span></span>

<span data-ttu-id="e4e7c-154">Talvez seja necessário aumentar o tamanho do log dependendo de quantos eventos você deseja ver.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-154">You may need to increase the log size depending on how many events you want to see.</span></span> <span data-ttu-id="e4e7c-155">Uma desvantagem de usar o Visualizador de Eventos para o rastreamento de Winsock é que ele não carrega todos os recursos de cadeia de caracteres, de modo que as mensagens exibidas no campo Descrição (depois que você seleciona um evento) às vezes são difíceis de serem lidas (um argumento que deve ser formatado como hex será exibido em decimal, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="e4e7c-155">One drawback to using the Event Viewer for Winsock tracing is that it does not load all the string resources so the messages displayed in the Description field (once you select an event) is sometimes hard to read (an argument that should be formatted as hex will be displayed in decimal, for example).</span></span> <span data-ttu-id="e4e7c-156">No entanto, você pode selecionar a guia **detalhes** na descrição do evento que mostra a entrada de log XML bruto que geralmente tem mais facilidade para entender os argumentos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-156">However, you can select the **Details** tab in the event description which shows the raw XML log entry which usually has easier to understand arguments.</span></span>

## <a name="interpreting-winsock-tracing-logs"></a><span data-ttu-id="e4e7c-157">Interpretando logs de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-157">Interpreting Winsock Tracing Logs</span></span>

<span data-ttu-id="e4e7c-158">Todos os eventos de rastreamento do Winsock em um log contêm dois tipos de informações:</span><span class="sxs-lookup"><span data-stu-id="e4e7c-158">All Winsock tracing events in a log contain two types of information:</span></span>

-   <span data-ttu-id="e4e7c-159">Sistema</span><span class="sxs-lookup"><span data-stu-id="e4e7c-159">System</span></span>
-   <span data-ttu-id="e4e7c-160">EventData</span><span class="sxs-lookup"><span data-stu-id="e4e7c-160">EventData</span></span>

<span data-ttu-id="e4e7c-161">As informações do sistema contêm o nível de log, a hora em que a entrada de log foi criada, a ID do evento que representa o tipo de evento, a ID do processo de execução, a ID do thread de execução e outras informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-161">The system information contains the logging level, the time the log entry was created, the event ID that represents the event type, the execution Process ID, the execution Thread ID, and other system information.</span></span> <span data-ttu-id="e4e7c-162">Um nível de log de 4 no rastreamento do Winsock representa o log de eventos de informações.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-162">A log level of 4 in Winsock tracing represents information event logging.</span></span> <span data-ttu-id="e4e7c-163">Um nível de log de 5 no rastreamento de Winsock representa o log de eventos detalhado.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-163">A log level of 5 in Winsock tracing represents verbose event logging.</span></span>

<span data-ttu-id="e4e7c-164">A ID do processo de execução e a ID do thread nas informações do sistema indicam o processo e o thread que estava em execução quando o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-164">The execution process ID and thread ID in the system information indicates the process and thread that was running when the event occurred.</span></span> <span data-ttu-id="e4e7c-165">Em muitos casos, isso representará um kernel ou thread de trabalho e processo, não um thread de modo de usuário e ou o processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-165">In many cases, this will represent a kernel or worker thread and process, not a user-mode thread and or the process of the application.</span></span> <span data-ttu-id="e4e7c-166">Portanto, esse campo normalmente não é muito útil.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-166">So this field is normally not very useful.</span></span>

<span data-ttu-id="e4e7c-167">Cada tipo de evento de rastreamento do Winsock tem uma ID de evento exclusiva na seção do sistema dos dados registrados.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-167">Each Winsock tracing event type has a unique event ID in the system section of the logged data.</span></span> <span data-ttu-id="e4e7c-168">Essas IDs de evento podem ser facilmente usadas para filtrar um arquivo de log para eventos de rastreamento Winsock específicos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-168">These event IDs can easily be used to filter a log file for specific Winsock tracing events.</span></span>

<span data-ttu-id="e4e7c-169">O EventData contém informações específicas para o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-169">The eventdata contains information specific to the event type.</span></span>

<span data-ttu-id="e4e7c-170">O parâmetro Process nas informações de EVENTDATA é o endereço da estrutura EPROCESS do kernel para o processo, não o PID real.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-170">The Process parameter in the eventdata information is the kernel EPROCESS structure address for the process, not the actual PID.</span></span> <span data-ttu-id="e4e7c-171">Para corresponder um evento à PID do modo de usuário, pegue o valor do processo das informações de EVENTDATA de qualquer entrada de log e examine antes no log um evento de criação de soquete com o valor do processo.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-171">To match an event to the user mode PID, take the Process value from the eventdata information from any log entry and look earlier in the log for a socket creation event with the Process value.</span></span> <span data-ttu-id="e4e7c-172">Quando uma correspondência é encontrada, o último parâmetro nos dados de evento de criação de soquete é a ID de processo do modo de usuário que criou o soquete.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-172">Once a match is found, the last parameter in the socket creation event data is the user-mode Process ID that created the socket.</span></span>

<span data-ttu-id="e4e7c-173">Um parâmetro de endereço nas informações de EVENTDATA é retornado em alguns eventos de rastreamento do Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-173">An Address parameter in the eventdata information is returned in some Winsock tracing events.</span></span> <span data-ttu-id="e4e7c-174">Um parâmetro de endereço representa um endereço IP, mas é exibido no arquivo de texto criado pela ferramenta de **tracerpt.exe** ou em Visualizador de eventos como bytes brutos ou um número.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-174">An Address parameter represents an IP address, but it is displayed in the text file created by the **tracerpt.exe** tool or in Event Viewer as raw bytes or a number.</span></span> <span data-ttu-id="e4e7c-175">Os endereços IPv6 são exibidos em hexadecimal, para que sejam compreendidos com mais facilidade.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-175">IPv6 addresses are displayed in hexadecimal, so they are more easily understood.</span></span> <span data-ttu-id="e4e7c-176">Os endereços IPv4 são exibidos como um número decimal grande.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-176">IPv4 addresses are displayed as a large decimal number.</span></span> <span data-ttu-id="e4e7c-177">Os desenvolvedores precisarão converter manualmente os bytes brutos de um endereço IPv4 para a notação de endereço decimal de IPv4 pontilhado e mais familiar para ser mais capaz de interpretar o valor.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-177">Developers will need to manually convert the raw bytes of an IPv4 address to the more familiar IPv4 dotted-decimal address notation to be better able to interpret the value.</span></span>

<span data-ttu-id="e4e7c-178">Um parâmetro de erro no EVENTDATA é retornado em alguns eventos de rastreamento do Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-178">An Error parameter in the eventdata is returned in some Winsock tracing events.</span></span> <span data-ttu-id="e4e7c-179">Um parâmetro de erro é da forma de um código de erro NTSTATUS ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-179">An Error parameter is of the form of an NTSTATUS or HRESULT error code.</span></span> <span data-ttu-id="e4e7c-180">Esse parâmetro de erro é exibido no arquivo de texto criado pela ferramenta de **tracerpt.exe** ou no Visualizador de eventos como um número decimal.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-180">This error parameter is displayed in the text file created by the **tracerpt.exe** tool or in Event Viewer as a decimal number.</span></span> <span data-ttu-id="e4e7c-181">Os desenvolvedores precisarão converter manualmente o número decimal para um número hexadecimal a fim de interpretar melhor o código de erro em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="e4e7c-181">Developers will need to manually convert the decimal number to a hex number in order to better interpret the error code in some cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4e7c-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4e7c-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4e7c-183">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-183">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e4e7c-184">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-184">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="e4e7c-185">Detalhes de rastreamento de eventos de rede do Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-185">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="e4e7c-186">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="e4e7c-186">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
