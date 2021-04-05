---
description: A partir do Windows Vista, o serviço WMI não usa os arquivos de log do WMI. Em vez disso, ele usa o ETW (rastreamento de eventos para Windows) e os eventos estão disponíveis por meio de Visualizador de Eventos ou da ferramenta de linha de comando wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Rastreando a atividade WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662657"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="e7bfc-104">Rastreando a atividade WMI</span><span class="sxs-lookup"><span data-stu-id="e7bfc-104">Tracing WMI Activity</span></span>

<span data-ttu-id="e7bfc-105">A partir do Windows Vista, o serviço WMI não usa os [arquivos de log do WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="e7bfc-106">Em vez disso, ele usa o [ETW (rastreamento de eventos para Windows)](/windows/desktop/ETW/event-tracing-portal) e os eventos estão disponíveis por meio de **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="e7bfc-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="e7bfc-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e7bfc-108">Obtendo eventos WMI por meio de Visualizador de Eventos</span><span class="sxs-lookup"><span data-stu-id="e7bfc-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="e7bfc-109">Habilitando o rastreamento WMI no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="e7bfc-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="e7bfc-110">Usando o rastreamento WMI baseado em WPP</span><span class="sxs-lookup"><span data-stu-id="e7bfc-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="e7bfc-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7bfc-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="e7bfc-112">Obtendo eventos WMI por meio de Visualizador de Eventos</span><span class="sxs-lookup"><span data-stu-id="e7bfc-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="e7bfc-113">O arquivo WMITracing. log contém os eventos que o WMI rastreia.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="e7bfc-114">No entanto, esse é um arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-114">However, this is a binary file.</span></span> <span data-ttu-id="e7bfc-115">Para ver esses eventos em um formato legível pelos seres humanos, use o **Visualizador de eventos**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="e7bfc-116">Por padrão, os eventos WMI não são rastreados.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="e7bfc-117">Este procedimento descreve como usar **Visualizador de eventos** para habilitar o rastreamento de eventos WMI e localizar eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="e7bfc-118">Você pode fazer as mesmas operações por meio da ferramenta de linha de comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="e7bfc-119">**Para exibir eventos WMI no Visualizador de Eventos**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="e7bfc-120">Abra o **Visualizador de Eventos**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-120">Open **Event Viewer**.</span></span> <span data-ttu-id="e7bfc-121">No menu **Exibir** , clique em **Mostrar logs analíticos e de depuração**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="e7bfc-122">Localize o log do canal de **rastreamento** para WMI em aplicativos e logs de serviço \| atividade do WMI do Microsoft \| Windows \| .</span><span class="sxs-lookup"><span data-stu-id="e7bfc-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="e7bfc-123">Clique com o botão direito do mouse no log de **rastreamento** e selecione **Propriedades do log**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="e7bfc-124">Clique na caixa de seleção **habilitar registro em log** para iniciar o rastreamento de eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="e7bfc-125">Para obter mais informações sobre canais, consulte [logs de eventos e canais no log de eventos do Windows](/previous-versions//aa385225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="e7bfc-126">Os eventos WMI aparecem na janela de evento para a **atividade WMI**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="e7bfc-127">Clique duas vezes em um evento na lista para ver as informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="e7bfc-128">Você pode exibir um evento na **exibição XML** ou no formato de **exibição amigável** .</span><span class="sxs-lookup"><span data-stu-id="e7bfc-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="e7bfc-129">O campo **ID do evento** exibe um valor que contém as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="e7bfc-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Evento 1</span><span class="sxs-lookup"><span data-stu-id="e7bfc-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-131">Início da sequência de eventos para uma operação específica.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="e7bfc-132">Uma ocorrência para cada sequência.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="e7bfc-133">Os campos de evento de um evento 1 são:</span><span class="sxs-lookup"><span data-stu-id="e7bfc-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="e7bfc-134">**GroupOperationID** é um identificador exclusivo que é usado para todos os eventos relatados para um cliente específico.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="e7bfc-135">**OperationId** indica a sequência de operação.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="e7bfc-136">**Operation** especifica a conexão ou a solicitação ao WMI.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="e7bfc-137">O **usuário** indica a conta que faz uma solicitação ao WMI executando um script ou por meio do CIM Studio.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="e7bfc-138">**Namespace** mostra o namespace WMI para o qual a conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="e7bfc-139">Por exemplo, um script pode solicitar todas as instâncias de uma classe WMI, como o [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="e7bfc-140">A primeira operação pode ser uma conexão com o WMI.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="e7bfc-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Evento 2</span><span class="sxs-lookup"><span data-stu-id="e7bfc-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-142">Eventos que compõem a operação.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-142">Events that make up the operation.</span></span> <span data-ttu-id="e7bfc-143">Uma ou mais ocorrências na sequência.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="e7bfc-144">Os campos de evento para um evento 2 são:</span><span class="sxs-lookup"><span data-stu-id="e7bfc-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="e7bfc-145">**GroupOperationID** indica a sequência na qual o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="e7bfc-146">**GroupOperationID** indica a sequência na qual o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="e7bfc-147">**ProviderName** indica o nome do provedor que fornece os dados.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="e7bfc-148">**Path** é o caminho do WMI para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="e7bfc-149">Por exemplo, a operação pode ser uma enumeração do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="e7bfc-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Evento 3</span><span class="sxs-lookup"><span data-stu-id="e7bfc-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-151">Fim da sequência de eventos para uma operação específica.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="e7bfc-152">Uma ocorrência para cada sequência.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="e7bfc-153">Somente o **GroupOperationID** é mostrado.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="e7bfc-154">Habilitando o rastreamento WMI no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="e7bfc-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="e7bfc-155">Você também pode habilitar o rastreamento de eventos do WMI por meio da ferramenta de linha de comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="e7bfc-156">Use o seguinte comando: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="e7bfc-157">A origem do evento WMI é Microsoft-Windows-WMI.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="e7bfc-158">Para obter mais informações sobre Wevtutil.exe, consulte [sobre o log de eventos do Windows](/previous-versions//aa382610(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="e7bfc-159">Usando o rastreamento WMI baseado em WPP</span><span class="sxs-lookup"><span data-stu-id="e7bfc-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="e7bfc-160">Em sistemas operacionais Windows que começam com o Windows Vista, o WMI cria um canal de rastreamento ativo durante o processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="e7bfc-161">O nome do canal é sessão de \_ rastreamento do WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="e7bfc-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="e7bfc-162">Somente os erros são registrados no canal.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="e7bfc-163">O WPP (pré-processador de rastreamento de software) do Windows registra as informações em um arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="e7bfc-164">Para ler o arquivo, você deve primeiro convertê-lo em um formato de texto legível.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="e7bfc-165">Você usa uma ferramenta chamada tracefmt.exe do [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para fazer a tradução.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="e7bfc-166">A ferramenta requer informações armazenadas em alguns arquivos associados.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="e7bfc-167">Os arquivos estão localizados no diretório% SystemRoot% \\ System32 \\ WBEM \\ TMF e têm uma extensão de nome de arquivo. TMF.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="e7bfc-168">Na verdade, a ferramenta requer um único arquivo. TMF.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="e7bfc-169">Você torna esse único arquivo concatenando todos os arquivos. TMF em outro arquivo. TMF.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="e7bfc-170">Para obter mais informações sobre arquivos. TMF, consulte [arquivo de formato de mensagem de rastreamento](/windows-hardware/drivers/devtest/trace-message-format-file).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="e7bfc-171">Depois de instalar o [WDK (Kit de driver do Windows)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para obter as tracelog.exe e tracefmt.exe ferramentas de linha de comando, execute as etapas a seguir para coletar um rastreamento WMI baseado em WPP.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="e7bfc-172">**Para exibir um rastreamento WMI baseado em WPP**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="e7bfc-173">Para criar o arquivo. TMF único, abra uma janela de prompt de comandos com privilégios elevados e navegue até o diretório% SystemRoot% \\ System32 \\ WBEM \\ TMF.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="e7bfc-174">Digite **Copy/y% SystemRoot% \\ System32 \\ WBEM \\ TMF \\ \* . TMF% SystemRoot% \\ System32 \\ WBEM \\ TMF \\ WMI. TMF**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="e7bfc-175">Isso criará um arquivo chamado WMI. tmf que inclui o conteúdo de todos os outros arquivos. TMF.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="e7bfc-176">Digite **tracelog-liberar \_ \_ sessão de rastreamento WMI**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="e7bfc-177">Isso limpará os buffers de WPP no disco.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="e7bfc-178">Digite o **prefixo do formato do rastreamento de conjunto \_ \_ = \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! COMPname!:%! FUNC!: %2! s!)**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="e7bfc-179">A ferramenta tracefmt adiciona algumas informações padrão a cada mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="e7bfc-180">Você pode configurar quais informações são incluídas definindo a variável de \_ ambiente de prefixo do formato de rastreamento \_ .</span><span class="sxs-lookup"><span data-stu-id="e7bfc-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="e7bfc-181">Para saber mais sobre a sintaxe usada, confira o [prefixo da mensagem de rastreamento](https://msdn.microsoft.com/library/aa139695.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="e7bfc-182">Digite **tracefmt-TMF% SystemRoot% \\ System32 \\ WBEM \\ TMF \\ wmi. TMF-o OUTPUT.TXT% SystemRoot% \\ System32 \\ WBEM \\ registra \\ WMITracing. log**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="e7bfc-183">Isso executa a tradução do formato binário para o formato de texto legível.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="e7bfc-184">Digite **notepad% systemroot% \\ System32 \\ WBEM \\ TMF \\OUTPUT.TXT**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="e7bfc-185">Isso abrirá o arquivo de rastreamento no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="e7bfc-186">A seguir estão algumas outras tarefas relacionadas a WPP que talvez você precise executar.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="e7bfc-187">**Para parar o rastreamento WMI baseado em WPP**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="e7bfc-188">Digite **tracelog-parar \_ \_ sessão de rastreamento WMI**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="e7bfc-189">**Para iniciar o rastreamento WMI baseado em WPP**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="e7bfc-190">Digite **tracelog-iniciar \_ \_ sessão de rastreamento WMI-GUID \# 1FF6B227-2CA7-40F9-9A66-980EADAA602E-RT-nível 5-sinalizador 0X7-f mytrace. COMPARTIMENTO**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="e7bfc-191">**Windows Vista:** Por padrão, o rastreamento WMI baseado em WPP é definido como o nível 2, que inclui apenas mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="e7bfc-192">Para incluir também as mensagens informativas, defina o nível como 4.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="e7bfc-193">Todas as áreas do WMI são rastreadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="e7bfc-194">Há três áreas distintas que podem ser rastreadas: Core (Flag = 0x1), ESS (Flag = 0x2) e PROV (Flag = 0x4).</span><span class="sxs-lookup"><span data-stu-id="e7bfc-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="e7bfc-195">No comando iniciar acima, o **sinalizador 0x7** faz com que todas as três áreas sejam rastreadas.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="e7bfc-196">**Windows 7:** Por padrão, o rastreamento WMI baseado em WPP é desabilitado e definido como nível 0.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="e7bfc-197">Para usar o rastreamento WMI baseado em WPP, esse recurso deve ser habilitado e definido para o nível 2 para mensagens de erro ou nível 4 para mensagens de erro e informativas.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="e7bfc-198">**Para listar todas as sessões de rastreamento de WPP**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="e7bfc-199">Digite **tracelog-l**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="e7bfc-200">**Para listar informações sobre a sessão de rastreamento de WPP do WMI**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="e7bfc-201">Digite **tracelog-l \| findstr/i "WMI \_ trace"**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="e7bfc-202">**Para exibir os parâmetros da sessão de rastreamento do WMI WPP**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="e7bfc-203">Digite **a \_ \_ sessão de rastreamento WMI tracelog-q**.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7bfc-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7bfc-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7bfc-205">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="e7bfc-205">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="e7bfc-206">Arquivos de log do WMI</span><span class="sxs-lookup"><span data-stu-id="e7bfc-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
