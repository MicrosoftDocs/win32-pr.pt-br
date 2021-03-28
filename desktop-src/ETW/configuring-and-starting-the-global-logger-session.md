---
description: A sessão de rastreamento de eventos do agente global registra eventos que ocorrem no início do processo de inicialização do sistema operacional.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configurando e iniciando a sessão global de agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8692e1f7321acc163e48cda7e3323f3d24adc1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968043"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configurando e iniciando a sessão global de agente

A sessão de rastreamento de eventos do agente global registra eventos que ocorrem no início do processo de inicialização do sistema operacional. Aplicativos e drivers de dispositivo podem usar a sessão de agente global para capturar rastreamentos antes que o usuário faça logon. Observe que alguns drivers de dispositivo, como drivers de dispositivo de disco, não são carregados no momento em que a sessão global de agente é iniciada.

> [!Note]  
> Se você estiver criando uma sessão global de agente no Windows Vista, considere a criação de uma [sessão do agente de log autologger](configuring-and-starting-an-autologger-session.md) .

 

Você usa o registro para configurar a sessão global do agente de log. Adicione a chave **GlobalLogger** à seguinte chave do registro, se ainda não estiver presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

A tabela a seguir descreve os valores que você pode definir para a chave **GlobalLogger** . Você deve ter privilégios de administrador para especificar esses valores de registro. Os valores do registro afetam todos os provedores que registram eventos na sessão global do agente. O valor **inicial** é o único valor necessário para iniciar a sessão global do agente de log; todos os outros valores têm configurações padrão que serão usadas se o valor não estiver presente no registro. Normalmente, você deve usar os valores padrão. Se você especificar um valor que o ETW não tem suporte, o ETW substituirá o valor.



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Defina esse valor como 1 (ativado) para iniciar a sessão global de agente na próxima vez que o sistema for iniciado. Para interromper a inicialização da sessão, defina esse valor como 0 (desativado). <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O tamanho de cada buffer, em quilobytes. Esse valor deve ser menor que um megabyte. O ETW usa o tamanho da memória física para calcular esse valor. <br/></td>
</tr>
<tr class="odd">
<td><strong>Clocktype</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O temporizador a ser usado ao registrar em log o carimbo de data/hora para cada evento.
<ul>
<li>1 = valor do contador de desempenho (alta resolução)</li>
<li>2 = temporizador do sistema</li>
<li>3 = contador de ciclo de CPU</li>
</ul>
Para obter uma descrição de cada tipo de relógio, consulte o membro <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> O valor padrão é 1 (valor do contador de desempenho) no Windows Vista e posterior. Antes do Windows Vista, o valor padrão é 2 (temporizador do sistema).<br/></td>
</tr>
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>Use esse valor para habilitar um ou mais provedores de kernel. Se você habilitar provedores de kernel, a sessão de agente global será renomeada para NT kernel logger quando ele for iniciado. Para obter os valores possíveis, consulte o membro <strong>EnableFlags</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>Contador de filecounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número de arquivos de log de rastreamento de eventos gerados por sessões de agente global. O sistema incrementa esse valor até atingir o valor de <strong>FileMax</strong>. Em seguida, ele redefine o valor para 0. Esse contador impede que o sistema substitua um arquivo de log de rastreamento de agente global. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número máximo de arquivos de log de rastreamento de eventos permitidos no sistema. Quando o número de logs de rastreamento atinge o máximo especificado, o sistema começa a substituir os logs, começando com o mais antigo. <br/> Se o arquivo de log especificado em <strong>filename</strong> existir, o ETW acrescentará o valor <strong>filecounterer</strong> ao nome do arquivo. Por exemplo, se o nome do arquivo de log padrão for usado, o formulário será%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br/> O valor padrão é 0, o que significa que não há nenhum máximo. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Caminho totalmente qualificado do arquivo de log. O caminho para esse arquivo deve existir. O arquivo de log é um arquivo de log sequencial. Observe que todos os provedores que gravam eventos na sessão do agente global gravam eventos nesse arquivo de log. O caminho é limitado a 1024 caracteres. Se <strong>filename</strong> não for especificado, os eventos serão gravados em%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>Antes do Windows Vista:</strong> O arquivo padrão é%SystemRoot%\System32\LogFiles\WMI\Trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Com que frequência, em segundos, os buffers de rastreamento são liberados forçosamente. O tempo de liberação mínimo é de 1 segundo. Essa liberação forçada é além da liberação automática que ocorre quando um buffer está cheio e quando a sessão de rastreamento é interrompida. <br/> Para o caso de um agente em tempo real, um valor igual a zero (o valor padrão) significa que o tempo de liberação será definido como 1 segundo. Um agente de log em tempo real é quando <strong>LOGFILEMODE</strong> é definido como <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> O valor padrão é 0. Por padrão, os buffers são liberados somente quando estão cheios. <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFilemode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifica as opções de sessão de log. Para valores, consulte <a href="logging-mode-constants.md">constantes do modo de log</a>. Esses valores têm suporte no Windows Vista e versões posteriores. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número máximo de buffers a serem alocados. Normalmente, esse valor é o número mínimo de buffers, mais vinte. O ETW usa o tamanho do buffer e o tamanho da memória física para calcular esse valor. Esse valor deve ser maior ou igual ao valor de <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>Cedido</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O tamanho máximo, em megabytes, do arquivo de log de rastreamento de eventos. Por padrão, não há nenhum tamanho máximo de arquivo.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número mínimo de buffers a serem alocados quando a sessão global do agente é iniciada. O número mínimo de buffers que você pode especificar é de dois buffers por processador. Por exemplo, em um único computador de processador, o número mínimo de buffers é dois. <br/> O valor padrão em um sistema de processador único é 0x3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O status de inicialização do agente de log global. Se o agente de log global não for iniciado, o valor dessa chave será o código de erro Win32 apropriado. Se o agente global for iniciado com êxito, o valor dessa chave será ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Depois que o registro tiver sido modificado e o computador for reiniciado, a sessão global do agente iniciará automaticamente e será usada como qualquer outra sessão com uma exceção: você usará o \_ identificador constante de ID do agente de log global do WMI \_ \_ (definido em Wmistr. h) para fazer referência à sessão global do agente. Essa constante pode ser usada como um argumento para qualquer função de rastreamento de eventos que aceite um identificador de sessão. Em funções que aceitam um nome de sessão, use o \_ nome do agente de log global \_ .

O controlador de agente global não chama a função [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar provedores. O provedor é responsável por determinar se a sessão global do agente de log foi iniciada e, em seguida, habilitá-la.

Para determinar se a sessão global de agente de log foi iniciada, você pode chamar a função [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) , definindo *SessionHandle* como \_ ID do agente global WMI \_ \_ e *ControlCode* para consulta de **controle de rastreamento de eventos \_ \_ \_**. Se a chamada **ControlTrace** for bem-sucedida, a sessão global de agente existirá e o provedor poderá habilitar a si mesmo e registrar eventos na sessão global do agente (a função **ControlTrace** retornará uma instância WMI de erro \_ \_ \_ não \_ encontrada se o agente de log global não estiver ativo).

Normalmente, o controlador é responsável por passar os sinalizadores de habilitação e o nível para o provedor quando ele habilita o provedor, mas como o controlador de agente global não habilita o provedor, é responsabilidade do provedor passar essas informações para si mesmo, se necessário.

A sessão global do agente é um recurso limitado e deve ser usada com moderação. Os serviços que desejam capturar informações durante o processo de inicialização devem considerar a adição da lógica do controlador a si só, em vez de usar a sessão global do agente de log.

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão de agente de log particular, consulte [Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do agente do NT kernel, consulte [Configurando e iniciando a sessão do agente de log do NT](configuring-and-starting-the-nt-kernel-logger-session.md).

