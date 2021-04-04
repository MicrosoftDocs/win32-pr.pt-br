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
# <a name="record-and-view-tracelogging-events"></a>Registrar e exibir eventos de TraceLogging

Registre eventos do TraceLogging com o gravador de desempenho do Windows (WPR) e exiba-os com o Windows Performance Analyzer (WPA).

## <a name="prerequisites"></a>Pré-requisitos

-   Windows 10
-   A versão Windows 10 do gravador de desempenho do Windows (WPR) e a versão do Windows 10 do Windows Performance Analyzer (WPA) que faz parte do Windows ADK (Kit de avaliação e implantação do® Windows).

> [!IMPORTANT]
> Os rastreamentos capturados com TraceLogging devem ser capturados com a versão do Windows 10 do gravador de desempenho do Windows e exibidos com a versão do Windows 10 do analisador de desempenho do Windows. Se não for possível capturar ou decodificar seus eventos, verifique se você está usando a versão do Windows 10 das ferramentas.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. capturar dados de rastreamento com WPR

Para capturar um rastreamento em Windows Phone, consulte capturar eventos do TraceLogging no Windows Phone abaixo.

Crie um perfil do gravador de desempenho do Windows (. wprp) para que você possa usar o WPR para capturar seus eventos do Tracelogging.

**Crie um. Arquivo WPRP**

1.  Use o exemplo de WPRP a seguir com o exemplo de código nativo no [TraceLogging C/C++ início rápido](tracelogging-native-quick-start.md) ou o exemplo gerenciado no [início rápido gerenciado TraceLogging](tracelogging-managed-quick-start.md). Se você estiver registrando eventos de seu próprio provedor, substitua as `TODO` seções pelos valores apropriados para seu provedor.

    > \[! Fundamental\]  

     

    Se você estiver usando o início rápido do TraceLogging C/C++, especifique o GUID do provedor no `Name` atributo do `<EventProvider>` elemento. Por exemplo: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Se você estiver usando o início rápido do TraceLogging gerenciado, especifique o nome do provedor precedido por ' \* ' no `Name` atributo do `<EventProvider />` elemento. Por exemplo, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    Arquivo WPRP de exemplo.

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

    

2.  Salve o arquivo com um. Extensão de nome de arquivo WPRP.
3.  Inicie a captura usando o WPR em uma janela de prompt de comando com privilégios elevados (executar como administrador).

    **<path to wpr>\\wpr.exe-Start GeneralProfile-Start TraceLoggingProvider. wprp**

    > \[! Dicas\]  
    > Para fins de criação de perfil gerais, você também pode adicionar **– iniciar o GeneralProfile** à linha de comando wpr.exe para capturar eventos do sistema junto com os eventos do seu provedor. Se você quiser apenas reunir seus eventos, omita **-Start GeneralProfile**.

     

4.  Execute o aplicativo que contém seus eventos.
5.  Pare a captura de rastreamento.

    **<path to wpr>\\wpr.exe-Stop TraceCaptureFile. etl descrição**

    > \[! Dicas\]  
    > Se você adicionou **– inicie o GeneralProfile** para coletar eventos do sistema, adicione **-o GeneralProfile** à linha de comando **wpr.exe** acima.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. capturar eventos do TraceLogging em Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Inicie o tracelog para capturar eventos de seu provedor.

    **cmdd tracelog-start Test-f c: \\ Test. etl-GUID \# ProviderGuid**

2.  Execute o cenário de teste para registrar eventos.
3.  Pare a captura de rastreamento.

    **cmdd tracelog – parar teste**

4.  Mescle os resultados do rastreamento do sistema com os resultados do rastreamento.

    **cmdd Xperf-Merge c: \\ Test. etl c: \\ testmerged. etl**

5.  Recupere o arquivo de log mesclado.

    **getd c: \\ testmerged. etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. exibir dados do TraceLogging usando o analisador de desempenho do Windows.

Atualmente, o WPA é o único visualizador que você pode usar para exibir arquivos de rastreamento TraceLogging (. ETL).

1.  Inicie o WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults. etl**

2.  Carregue o arquivo de rastreamento (. ETL) que você especificou no comando wpa.exe acima, por exemplo, traceLoggingResults. etl.
3.  Exiba seus eventos de provedor. No Gerenciador de grafo do WPA, expanda **atividade do sistema**.
4.  Clique duas vezes no painel **eventos genéricos** para exibir os eventos no painel **análise** .

    ![expandir eventos genéricos](images/expandsystemactivity.png)

5.  No painel análise, localize os eventos do seu provedor para verificar se o TraceLogging está funcionando.

    Na coluna **nome do provedor** da tabela **eventos genéricos** , localize e selecione a linha com o nome do provedor.

    Se você tiver vários provedores para classificar, clique no cabeçalho da coluna para classificar por nome de coluna, o que pode facilitar a localização do seu provedor.

    Quando você encontrar seu provedor, clique com o botão direito do mouse no nome e selecione **filtrar para seleção**.

    ![filtrar seleção para provedor](images/filtertoselection.png)

    O evento para SimpleTraceLoggingProvider e seu valor aparecerão no painel inferior da janela de análise. Expanda o nome do provedor para ver os eventos.

    ![exibir o evento do simpletraceloggingprovider](images/eventview.png)

    Para obter mais informações sobre como usar o WPA, consulte [analisador de desempenho do Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

O processo de gravação e exibição de eventos ETW usando WPR e WPA se aplica igualmente bem aos eventos TraceLogging.

Consulte [exemplos de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md) para obter exemplos de Tracelogging adicionais.

 

 