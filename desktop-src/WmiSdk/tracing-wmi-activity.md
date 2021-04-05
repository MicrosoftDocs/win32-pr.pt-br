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
# <a name="tracing-wmi-activity"></a>Rastreando a atividade WMI

A partir do Windows Vista, o serviço WMI não usa os [arquivos de log do WMI](wmi-log-files.md). Em vez disso, ele usa o [ETW (rastreamento de eventos para Windows)](/windows/desktop/ETW/event-tracing-portal) e os eventos estão disponíveis por meio de **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil.

As seções a seguir são discutidas neste tópico:

-   [Obtendo eventos WMI por meio de Visualizador de Eventos](#obtaining-wmi-events-through-event-viewer)
-   [Habilitando o rastreamento WMI no prompt de comando](#enabling-wmi-tracing-at-command-prompt)
-   [Usando o rastreamento WMI baseado em WPP](#using-wpp-based-wmi-tracing)
-   [Tópicos relacionados](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a>Obtendo eventos WMI por meio de Visualizador de Eventos

O arquivo WMITracing. log contém os eventos que o WMI rastreia. No entanto, esse é um arquivo binário. Para ver esses eventos em um formato legível pelos seres humanos, use o **Visualizador de eventos**.

Por padrão, os eventos WMI não são rastreados. Este procedimento descreve como usar **Visualizador de eventos** para habilitar o rastreamento de eventos WMI e localizar eventos WMI. Você pode fazer as mesmas operações por meio da ferramenta de linha de comando wevtutil.

**Para exibir eventos WMI no Visualizador de Eventos**

1.  Abra o **Visualizador de Eventos**. No menu **Exibir** , clique em **Mostrar logs analíticos e de depuração**. Localize o log do canal de **rastreamento** para WMI em aplicativos e logs de serviço \| atividade do WMI do Microsoft \| Windows \| .
2.  Clique com o botão direito do mouse no log de **rastreamento** e selecione **Propriedades do log**. Clique na caixa de seleção **habilitar registro em log** para iniciar o rastreamento de eventos WMI. Para obter mais informações sobre canais, consulte [logs de eventos e canais no log de eventos do Windows](/previous-versions//aa385225(v=vs.85)).
3.  Os eventos WMI aparecem na janela de evento para a **atividade WMI**. Clique duas vezes em um evento na lista para ver as informações detalhadas. Você pode exibir um evento na **exibição XML** ou no formato de **exibição amigável** .

O campo **ID do evento** exibe um valor que contém as informações a seguir.

<dl> <dt>

<span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Evento 1
</dt> <dd>

Início da sequência de eventos para uma operação específica. Uma ocorrência para cada sequência.

Os campos de evento de um evento 1 são:

-   **GroupOperationID** é um identificador exclusivo que é usado para todos os eventos relatados para um cliente específico.
-   **OperationId** indica a sequência de operação.
-   **Operation** especifica a conexão ou a solicitação ao WMI.
-   O **usuário** indica a conta que faz uma solicitação ao WMI executando um script ou por meio do CIM Studio.
-   **Namespace** mostra o namespace WMI para o qual a conexão é feita.

Por exemplo, um script pode solicitar todas as instâncias de uma classe WMI, como o [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service). A primeira operação pode ser uma conexão com o WMI.

</dd> <dt>

<span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Evento 2
</dt> <dd>

Eventos que compõem a operação. Uma ou mais ocorrências na sequência.

Os campos de evento para um evento 2 são:

-   **GroupOperationID** indica a sequência na qual o evento ocorre.
-   **GroupOperationID** indica a sequência na qual o evento ocorre.
-   **ProviderName** indica o nome do provedor que fornece os dados.
-   **Path** é o caminho do WMI para o objeto.

Por exemplo, a operação pode ser uma enumeração do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

<span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Evento 3
</dt> <dd>

Fim da sequência de eventos para uma operação específica. Uma ocorrência para cada sequência.

Somente o **GroupOperationID** é mostrado.

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a>Habilitando o rastreamento WMI no prompt de comando

Você também pode habilitar o rastreamento de eventos do WMI por meio da ferramenta de linha de comando wevtutil. Use o seguinte comando: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**. A origem do evento WMI é Microsoft-Windows-WMI. Para obter mais informações sobre Wevtutil.exe, consulte [sobre o log de eventos do Windows](/previous-versions//aa382610(v=vs.85)).

## <a name="using-wpp-based-wmi-tracing"></a>Usando o rastreamento WMI baseado em WPP

Em sistemas operacionais Windows que começam com o Windows Vista, o WMI cria um canal de rastreamento ativo durante o processo de inicialização. O nome do canal é sessão de \_ rastreamento do WMI \_ . Somente os erros são registrados no canal.

O WPP (pré-processador de rastreamento de software) do Windows registra as informações em um arquivo binário. Para ler o arquivo, você deve primeiro convertê-lo em um formato de texto legível. Você usa uma ferramenta chamada tracefmt.exe do [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para fazer a tradução. A ferramenta requer informações armazenadas em alguns arquivos associados. Os arquivos estão localizados no diretório% SystemRoot% \\ System32 \\ WBEM \\ TMF e têm uma extensão de nome de arquivo. TMF. Na verdade, a ferramenta requer um único arquivo. TMF. Você torna esse único arquivo concatenando todos os arquivos. TMF em outro arquivo. TMF. Para obter mais informações sobre arquivos. TMF, consulte [arquivo de formato de mensagem de rastreamento](/windows-hardware/drivers/devtest/trace-message-format-file).

Depois de instalar o [WDK (Kit de driver do Windows)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para obter as tracelog.exe e tracefmt.exe ferramentas de linha de comando, execute as etapas a seguir para coletar um rastreamento WMI baseado em WPP.

**Para exibir um rastreamento WMI baseado em WPP**

1.  Para criar o arquivo. TMF único, abra uma janela de prompt de comandos com privilégios elevados e navegue até o diretório% SystemRoot% \\ System32 \\ WBEM \\ TMF.

2.  Digite **Copy/y% SystemRoot% \\ System32 \\ WBEM \\ TMF \\ \* . TMF% SystemRoot% \\ System32 \\ WBEM \\ TMF \\ WMI. TMF**. Isso criará um arquivo chamado WMI. tmf que inclui o conteúdo de todos os outros arquivos. TMF.

3.  Digite **tracelog-liberar \_ \_ sessão de rastreamento WMI**. Isso limpará os buffers de WPP no disco.
4.  Digite o **prefixo do formato do rastreamento de conjunto \_ \_ = \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! COMPname!:%! FUNC!: %2! s!)**. A ferramenta tracefmt adiciona algumas informações padrão a cada mensagem de rastreamento. Você pode configurar quais informações são incluídas definindo a variável de \_ ambiente de prefixo do formato de rastreamento \_ . Para saber mais sobre a sintaxe usada, confira o [prefixo da mensagem de rastreamento](https://msdn.microsoft.com/library/aa139695.aspx).
5.  Digite **tracefmt-TMF% SystemRoot% \\ System32 \\ WBEM \\ TMF \\ wmi. TMF-o OUTPUT.TXT% SystemRoot% \\ System32 \\ WBEM \\ registra \\ WMITracing. log**. Isso executa a tradução do formato binário para o formato de texto legível.
6.  Digite **notepad% systemroot% \\ System32 \\ WBEM \\ TMF \\OUTPUT.TXT**. Isso abrirá o arquivo de rastreamento no bloco de notas.

A seguir estão algumas outras tarefas relacionadas a WPP que talvez você precise executar.

**Para parar o rastreamento WMI baseado em WPP**

-   Digite **tracelog-parar \_ \_ sessão de rastreamento WMI**.

**Para iniciar o rastreamento WMI baseado em WPP**

-   Digite **tracelog-iniciar \_ \_ sessão de rastreamento WMI-GUID \# 1FF6B227-2CA7-40F9-9A66-980EADAA602E-RT-nível 5-sinalizador 0X7-f mytrace. COMPARTIMENTO**

**Windows Vista:** Por padrão, o rastreamento WMI baseado em WPP é definido como o nível 2, que inclui apenas mensagens de erro. Para incluir também as mensagens informativas, defina o nível como 4. Todas as áreas do WMI são rastreadas por padrão. Há três áreas distintas que podem ser rastreadas: Core (Flag = 0x1), ESS (Flag = 0x2) e PROV (Flag = 0x4). No comando iniciar acima, o **sinalizador 0x7** faz com que todas as três áreas sejam rastreadas.

**Windows 7:** Por padrão, o rastreamento WMI baseado em WPP é desabilitado e definido como nível 0. Para usar o rastreamento WMI baseado em WPP, esse recurso deve ser habilitado e definido para o nível 2 para mensagens de erro ou nível 4 para mensagens de erro e informativas.

**Para listar todas as sessões de rastreamento de WPP**

-   Digite **tracelog-l**.

**Para listar informações sobre a sessão de rastreamento de WPP do WMI**

-   Digite **tracelog-l \| findstr/i "WMI \_ trace"**.

**Para exibir os parâmetros da sessão de rastreamento do WMI WPP**

-   Digite **a \_ \_ sessão de rastreamento WMI tracelog-q**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Arquivos de log do WMI](wmi-log-files.md)
</dt> </dl>

 

 
