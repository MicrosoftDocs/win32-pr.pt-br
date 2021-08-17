---
description: A sessão de rastreamento de eventos do Global Logger registra eventos que ocorrem no início do processo de inicialização do sistema operacional.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configurando e iniciando a sessão do global logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc15ad9fdb5150a976b9d7bccfb6315649617271c5ece2a7c676fbdb9f6f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395491"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configurando e iniciando a sessão do global logger

A sessão de rastreamento de eventos do Global Logger registra eventos que ocorrem no início do processo de inicialização do sistema operacional. Os aplicativos e drivers de dispositivo podem usar a sessão do Global Logger para capturar rastreamentos antes que o usuário entre. Observe que alguns drivers de dispositivo, como drivers de dispositivo de disco, não são carregados no momento em que a sessão do Global Logger é iniciada.

> [!Note]  
> Se você estiver criando uma sessão do Global Logger no Windows Vista, considere a criação de uma [sessão do AutoLogger.](configuring-and-starting-an-autologger-session.md)

 

Use o Registro para configurar a sessão do Global Logger. Adicione a **chave GlobalLogger** à seguinte chave do Registro, se ela ainda não estiver presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

A tabela a seguir descreve os valores que você pode definir para a **chave GlobalLogger.** Você deve ter privilégios de administrador para especificar esses valores do Registro. Os valores do Registro afetam todos os provedores que registram eventos na sessão do Global Logger. O **valor** Iniciar é o único valor necessário para iniciar a sessão do Global Logger; todos os outros valores terão configurações padrão que serão usadas se o valor não estiver presente no Registro. Normalmente, você deve usar os valores padrão. Se você especificar um valor ao qual o ETW não pode dar suporte, o ETW substituirá o valor.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>De definir esse valor como 1 (on) para iniciar a sessão do Global Logger na próxima vez que o sistema iniciar. Para interromper o início da sessão, de definido esse valor como 0 (desligado). <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O tamanho de cada buffer, em quilobytes. Esse valor deve ser menor que um megabyte. O ETW usa o tamanho da memória física para calcular esse valor. <br/></td>
</tr>
<tr class="odd">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O temporizador a ser usado ao registrar o carimbo de data/hora para cada evento.
<ul>
<li>1 = Valor do contador de desempenho (alta resolução)</li>
<li>2 = Temporizador do sistema</li>
<li>3 = Contador de ciclo de CPU</li>
</ul>
Para ver uma descrição de cada tipo de relógio, consulte <strong>o membro ClientContext</strong> <a href="wnode-header.md"><strong>do WNODE_HEADER</strong></a>.<br/> O valor padrão é 1 (valor do contador de desempenho) no Windows Vista e posterior. Antes de Windows Vista, o valor padrão é 2 (temporizador do sistema).<br/></td>
</tr>
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>Use esse valor para habilitar um ou mais provedores de kernel. Se você habilitar provedores de kernel, a sessão do Global Logger será renomeada como NT Kernel Logger quando ela for iniciada. Para valores possíveis, consulte <strong>o membro EnableFlags</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>do EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número de arquivos de log de rastreamento de eventos gerados por sessões do Global Logger. O sistema incrementa esse valor até atingir o valor <strong>de FileMax.</strong> Em seguida, ele redefine o valor para 0. Esse contador impede que o sistema sobrescreva um arquivo de log de rastreamento do Global Logger. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número máximo de arquivos de log de rastreamento de eventos permitidos no sistema. Quando o número de logs de rastreamento atinge o máximo especificado, o sistema começa a substituir os logs, começando com o mais antigo. <br/> Se o arquivo de log especificado em <strong>FileName</strong> existir, ETW anexa o valor <strong>FileCounter</strong> ao nome do arquivo. Por exemplo, se o nome do arquivo de log padrão for usado, o formulário será %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNNNN. <br/> O valor padrão é 0, o que significa que não há nenhum máximo. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Caminho totalmente qualificado do arquivo de log. O caminho para esse arquivo deve existir. O arquivo de log é um arquivo de log sequencial. Observe que todos os provedores que escrevem eventos na sessão do Global Logger escrevem eventos nesse arquivo de log. O caminho é limitado a 1024 caracteres. Se <strong>FileName</strong> não for especificado, os eventos serão gravados em %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>Antes do Windows Vista:</strong> O arquivo padrão é %SystemRoot%\System32\LogFiles\WMI\Trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Com que frequência, em segundos, os buffers de rastreamento são liberados à força. O tempo mínimo de liberação é de 1 segundo. Essa liberação forçada é além da liberação automática que ocorre quando um buffer está cheio e quando a sessão de rastreamento é interrompida. <br/> Para o caso de um logger em tempo real, um valor de zero (o valor padrão) significa que o tempo de liberação será definido como 1 segundo. Um loggger em tempo real é quando <strong>LogFileMode</strong> é definido <strong>como EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> O valor padrão é 0. Por padrão, os buffers são liberados somente quando estão completos. <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifica as opções de sessão de log. Para valores, consulte <a href="logging-mode-constants.md">Constantes de modo de registro em log.</a> Esses valores são suportados no Windows Vista e posterior. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número máximo de buffers a alocar. Normalmente, esse valor é o número mínimo de buffers mais vinte. O ETW usa o tamanho do buffer e o tamanho da memória física para calcular esse valor. Esse valor deve ser maior ou igual ao valor de <strong>MinimumBuffers.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O tamanho máximo, em megabytes, do arquivo de log de rastreamento de eventos. Por padrão, não há nenhum tamanho máximo de arquivo.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número mínimo de buffers a alocar quando a sessão do Agente Global é iniciada. O número mínimo de buffers que você pode especificar é dois buffers por processador. Por exemplo, em um único computador processador, o número mínimo de buffers é dois. <br/> O valor padrão em um sistema de processador único é 0x3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O status de inicialização do Global Logger. Se o Global Logger não conseguir iniciar, o valor dessa chave será o código de erro Win32 apropriado. Se o Global Logger for iniciado com êxito, o valor dessa chave será ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Depois que o Registro tiver sido modificado e o computador for reiniciado, a sessão do Global Logger será iniciada automaticamente e será usada como qualquer outra sessão com uma exceção: você usa o alçador constante de ID do WMI \_ GLOBAL \_ LOGGER (definido em Wmistr.h) para referenciar a sessão \_ do Global Logger. Essa constante pode ser usada como um argumento para qualquer função de rastreamento de eventos que aceite um alça de sessão. Em funções que aceitam um nome de sessão, use GLOBAL \_ LOGGER \_ NAME.

O controlador do Global Logger não chama a [**função EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar provedores. O provedor é responsável por determinar se a sessão do Global Logger foi iniciada e, em seguida, habilitando a si mesmo.

Para determinar se a sessão do Global Logger foi iniciada, você pode chamar a função [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) definindo *SessionHandle* como ID do WMI GLOBAL LOGGER e ControlCode como \_ EVENT TRACE CONTROL \_ \_ **\_ \_ \_ QUERY**.  Se a chamada **controlTrace** for bem-sucedida, a sessão do Global Logger existirá e o provedor poderá habilitar a si mesmo e registrar eventos na sessão do Global Logger (a **função ControlTrace** retornará ERROR WMI INSTANCE NOT FOUND se o Global Logger não \_ estiver \_ \_ \_ ativo).

Normalmente, o controlador é responsável por passar os sinalizadores de habilitar e o nível para o provedor quando ele habilita o provedor, mas como o controlador do Global Logger não habilita o provedor, é responsabilidade do provedor passar essas informações para ele mesmo, se necessário.

A sessão do Global Logger é um recurso limitado e deve ser usada com moderação. Os serviços que querem capturar informações durante o processo de inicialização devem considerar adicionar a lógica do controlador a si mesmo em vez de usar a sessão do Global Logger.

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão de logger privado, consulte [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do NT Kernel Logger, consulte Configurando e iniciando a [sessão do NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md).

