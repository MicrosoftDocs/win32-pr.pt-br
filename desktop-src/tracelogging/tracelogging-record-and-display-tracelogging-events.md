---
title: Registrar e exibir eventos de TraceLogging
description: Registre eventos do TraceLogging com o gravador de desempenho do Windows (WPR) e exiba-os com o Windows Performance Analyzer (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823963"
---
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="3d710-103">Registrar e exibir eventos de TraceLogging</span><span class="sxs-lookup"><span data-stu-id="3d710-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="3d710-104">Registre eventos do TraceLogging com o gravador de desempenho do Windows (WPR) e exiba-os com o Windows Performance Analyzer (WPA).</span><span class="sxs-lookup"><span data-stu-id="3d710-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3d710-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="3d710-105">Prerequisites</span></span>

-   <span data-ttu-id="3d710-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3d710-106">Windows 10</span></span>
-   <span data-ttu-id="3d710-107">A versão Windows 10 do gravador de desempenho do Windows (WPR) e a versão do Windows 10 do Windows Performance Analyzer (WPA) que faz parte do Windows ADK (Kit de avaliação e implantação do® Windows).</span><span class="sxs-lookup"><span data-stu-id="3d710-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d710-108">Os rastreamentos capturados com TraceLogging devem ser capturados com a versão do Windows 10 do gravador de desempenho do Windows e exibidos com a versão do Windows 10 do analisador de desempenho do Windows.</span><span class="sxs-lookup"><span data-stu-id="3d710-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="3d710-109">Se não for possível capturar ou decodificar seus eventos, verifique se você está usando a versão do Windows 10 das ferramentas.</span><span class="sxs-lookup"><span data-stu-id="3d710-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="3d710-110">1. capturar dados de rastreamento com WPR</span><span class="sxs-lookup"><span data-stu-id="3d710-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="3d710-111">Para capturar um rastreamento em Windows Phone, consulte capturar eventos do TraceLogging no Windows Phone abaixo.</span><span class="sxs-lookup"><span data-stu-id="3d710-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="3d710-112">Crie um perfil do gravador de desempenho do Windows (. wprp) para que você possa usar o WPR para capturar seus eventos do Tracelogging.</span><span class="sxs-lookup"><span data-stu-id="3d710-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="3d710-113">**Crie um. Arquivo WPRP**</span><span class="sxs-lookup"><span data-stu-id="3d710-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="3d710-114">Use o exemplo de WPRP a seguir com o exemplo de código nativo no [TraceLogging C/C++ início rápido](tracelogging-native-quick-start.md) ou o exemplo gerenciado no [início rápido gerenciado TraceLogging](tracelogging-managed-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="3d710-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="3d710-115">Se você estiver registrando eventos de seu próprio provedor, substitua as `TODO` seções pelos valores apropriados para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="3d710-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="3d710-116">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="3d710-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="3d710-117">Se você estiver usando o início rápido do TraceLogging C/C++, especifique o GUID do provedor no `Name` atributo do `<EventProvider>` elemento.</span><span class="sxs-lookup"><span data-stu-id="3d710-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="3d710-118">Por exemplo: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span><span class="sxs-lookup"><span data-stu-id="3d710-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="3d710-119">Se você estiver usando o início rápido do TraceLogging gerenciado, especifique o nome do provedor precedido por ' \* ' no `Name` atributo do `<EventProvider />` elemento.</span><span class="sxs-lookup"><span data-stu-id="3d710-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="3d710-120">Por exemplo, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span><span class="sxs-lookup"><span data-stu-id="3d710-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="3d710-121">Arquivo WPRP de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3d710-121">Sample WPRP file.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  <span data-ttu-id="3d710-122">Salve o arquivo com um. Extensão de nome de arquivo WPRP.</span><span class="sxs-lookup"><span data-stu-id="3d710-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="3d710-123">Inicie a captura usando o WPR em uma janela de prompt de comando com privilégios elevados (executar como administrador).</span><span class="sxs-lookup"><span data-stu-id="3d710-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="3d710-124">**<path to wpr>\\wpr.exe-Start GeneralProfile-Start TraceLoggingProvider. wprp**</span><span class="sxs-lookup"><span data-stu-id="3d710-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="3d710-125">\[! Dicas\]</span><span class="sxs-lookup"><span data-stu-id="3d710-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="3d710-126">Para fins de criação de perfil gerais, você também pode adicionar **– iniciar o GeneralProfile** à linha de comando wpr.exe para capturar eventos do sistema junto com os eventos do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="3d710-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="3d710-127">Se você quiser apenas reunir seus eventos, omita **-Start GeneralProfile**.</span><span class="sxs-lookup"><span data-stu-id="3d710-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="3d710-128">Execute o aplicativo que contém seus eventos.</span><span class="sxs-lookup"><span data-stu-id="3d710-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="3d710-129">Pare a captura de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="3d710-129">Stop the trace capture.</span></span>

    <span data-ttu-id="3d710-130">**<path to wpr>\\wpr.exe-Stop TraceCaptureFile. etl descrição**</span><span class="sxs-lookup"><span data-stu-id="3d710-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="3d710-131">\[! Dicas\]</span><span class="sxs-lookup"><span data-stu-id="3d710-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="3d710-132">Se você adicionou **– inicie o GeneralProfile** para coletar eventos do sistema, adicione **-o GeneralProfile** à linha de comando **wpr.exe** acima.</span><span class="sxs-lookup"><span data-stu-id="3d710-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="3d710-133">2. capturar eventos do TraceLogging em Windows Phone</span><span class="sxs-lookup"><span data-stu-id="3d710-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="3d710-134">Inicie o tracelog para capturar eventos de seu provedor.</span><span class="sxs-lookup"><span data-stu-id="3d710-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="3d710-135">**cmdd tracelog-start Test-f c: \\ Test. etl-GUID \# ProviderGuid**</span><span class="sxs-lookup"><span data-stu-id="3d710-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="3d710-136">Execute o cenário de teste para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="3d710-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="3d710-137">Pare a captura de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="3d710-137">Stop trace capture.</span></span>

    <span data-ttu-id="3d710-138">**cmdd tracelog – parar teste**</span><span class="sxs-lookup"><span data-stu-id="3d710-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="3d710-139">Mescle os resultados do rastreamento do sistema com os resultados do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="3d710-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="3d710-140">**cmdd Xperf-Merge c: \\ Test. etl c: \\ testmerged. etl**</span><span class="sxs-lookup"><span data-stu-id="3d710-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="3d710-141">Recupere o arquivo de log mesclado.</span><span class="sxs-lookup"><span data-stu-id="3d710-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="3d710-142">**getd c: \\ testmerged. etl**</span><span class="sxs-lookup"><span data-stu-id="3d710-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="3d710-143">3. exibir dados do TraceLogging usando o analisador de desempenho do Windows.</span><span class="sxs-lookup"><span data-stu-id="3d710-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="3d710-144">Atualmente, o WPA é o único visualizador que você pode usar para exibir arquivos de rastreamento TraceLogging (. ETL).</span><span class="sxs-lookup"><span data-stu-id="3d710-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="3d710-145">Inicie o WPA.</span><span class="sxs-lookup"><span data-stu-id="3d710-145">Start WPA.</span></span>

    <span data-ttu-id="3d710-146">**<path to wpr>\\wpa.exe traceLoggingResults. etl**</span><span class="sxs-lookup"><span data-stu-id="3d710-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="3d710-147">Carregue o arquivo de rastreamento (. ETL) que você especificou no comando wpa.exe acima, por exemplo, traceLoggingResults. etl.</span><span class="sxs-lookup"><span data-stu-id="3d710-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="3d710-148">Exiba seus eventos de provedor.</span><span class="sxs-lookup"><span data-stu-id="3d710-148">View your provider events.</span></span> <span data-ttu-id="3d710-149">No Gerenciador de grafo do WPA, expanda **atividade do sistema**.</span><span class="sxs-lookup"><span data-stu-id="3d710-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="3d710-150">Clique duas vezes no painel **eventos genéricos** para exibir os eventos no painel **análise** .</span><span class="sxs-lookup"><span data-stu-id="3d710-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![expandir eventos genéricos](images/expandsystemactivity.png)

5.  <span data-ttu-id="3d710-152">No painel análise, localize os eventos do seu provedor para verificar se o TraceLogging está funcionando.</span><span class="sxs-lookup"><span data-stu-id="3d710-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="3d710-153">Na coluna **nome do provedor** da tabela **eventos genéricos** , localize e selecione a linha com o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="3d710-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="3d710-154">Se você tiver vários provedores para classificar, clique no cabeçalho da coluna para classificar por nome de coluna, o que pode facilitar a localização do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="3d710-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="3d710-155">Quando você encontrar seu provedor, clique com o botão direito do mouse no nome e selecione **filtrar para seleção**.</span><span class="sxs-lookup"><span data-stu-id="3d710-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![filtrar seleção para provedor](images/filtertoselection.png)

    <span data-ttu-id="3d710-157">O evento para SimpleTraceLoggingProvider e seu valor aparecerão no painel inferior da janela de análise.</span><span class="sxs-lookup"><span data-stu-id="3d710-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="3d710-158">Expanda o nome do provedor para ver os eventos.</span><span class="sxs-lookup"><span data-stu-id="3d710-158">Expand the provider name to see the events.</span></span>

    ![exibir o evento do simpletraceloggingprovider](images/eventview.png)

    <span data-ttu-id="3d710-160">Para obter mais informações sobre como usar o WPA, consulte [analisador de desempenho do Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="3d710-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="3d710-161">Resumo e próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3d710-161">Summary and next steps</span></span>

<span data-ttu-id="3d710-162">O processo de gravação e exibição de eventos ETW usando WPR e WPA se aplica igualmente bem aos eventos TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="3d710-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="3d710-163">Consulte [exemplos de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md) para obter exemplos de Tracelogging adicionais.</span><span class="sxs-lookup"><span data-stu-id="3d710-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 