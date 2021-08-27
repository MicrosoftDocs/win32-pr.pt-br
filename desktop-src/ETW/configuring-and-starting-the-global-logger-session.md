---
description: A sessão de rastreamento de eventos do agente global registra eventos que ocorrem no início do processo de inicialização do sistema operacional.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configurando e iniciando a sessão global de agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a928cba5eb782ca4a57f7dba4776de79f42d7af
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477042"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configurando e iniciando a sessão global de agente

A sessão de rastreamento de eventos do agente global registra eventos que ocorrem no início do processo de inicialização do sistema operacional. Aplicativos e drivers de dispositivo podem usar a sessão de agente global para capturar rastreamentos antes que o usuário faça logon. Observe que alguns drivers de dispositivo, como drivers de dispositivo de disco, não são carregados no momento em que a sessão global de agente é iniciada.

> [!Note]  
> se você estiver criando uma sessão Global de agente no Windows Vista, considere a criação de uma [sessão do agente de log autologger](configuring-and-starting-an-autologger-session.md) em vez disso.

 

Você usa o registro para configurar a sessão global do agente de log. Adicione a chave **GlobalLogger** à seguinte chave do registro, se ainda não estiver presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

A tabela a seguir descreve os valores que você pode definir para a chave **GlobalLogger** . Você deve ter privilégios de administrador para especificar esses valores de registro. Os valores do registro afetam todos os provedores que registram eventos na sessão global do agente. O valor **inicial** é o único valor necessário para iniciar a sessão global do agente de log; todos os outros valores têm configurações padrão que serão usadas se o valor não estiver presente no registro. Normalmente, você deve usar os valores padrão. Se você especificar um valor que o ETW não tem suporte, o ETW substituirá o valor.




| Valor | Type | Descrição | 
|-------|------|-------------|
| <strong>Iniciar</strong> | <strong>REG_DWORD</strong> | Defina esse valor como 1 (ativado) para iniciar a sessão global de agente na próxima vez que o sistema for iniciado. Para interromper a inicialização da sessão, defina esse valor como 0 (desativado). <br /> | 
| <strong>BufferSize</strong> | <strong>REG_DWORD</strong> | O tamanho de cada buffer, em quilobytes. Esse valor deve ser menor que um megabyte. O ETW usa o tamanho da memória física para calcular esse valor. <br /> | 
| <strong>Clocktype</strong> | <strong>REG_DWORD</strong> | O temporizador a ser usado ao registrar em log o carimbo de data/hora para cada evento.<ul><li>1 = valor do contador de desempenho (alta resolução)</li><li>2 = temporizador do sistema</li><li>3 = contador de ciclo de CPU</li></ul>Para obter uma descrição de cada tipo de relógio, consulte o membro <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br /> o valor padrão é 1 (valor do contador de desempenho) no Windows Vista e posterior. antes do Windows Vista, o valor padrão é 2 (temporizador do sistema).<br /> | 
| <strong>EnableKernelFlags</strong> | <strong>REG_BINARY</strong> | Use esse valor para habilitar um ou mais provedores de kernel. Se você habilitar provedores de kernel, a sessão de agente global será renomeada para NT kernel logger quando ele for iniciado. Para obter os valores possíveis, consulte o membro <strong>EnableFlags</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br /> | 
| <strong>Contador de filecounter</strong> | <strong>REG_DWORD</strong> | O número de arquivos de log de rastreamento de eventos gerados por sessões de agente global. O sistema incrementa esse valor até atingir o valor de <strong>FileMax</strong>. Em seguida, ele redefine o valor para 0. Esse contador impede que o sistema substitua um arquivo de log de rastreamento de agente global. <br /> | 
| <strong>FileMax</strong> | <strong>REG_DWORD</strong> | O número máximo de arquivos de log de rastreamento de eventos permitidos no sistema. Quando o número de logs de rastreamento atinge o máximo especificado, o sistema começa a substituir os logs, começando com o mais antigo. <br /> Se o arquivo de log especificado em <strong>filename</strong> existir, o ETW acrescentará o valor <strong>filecounterer</strong> ao nome do arquivo. Por exemplo, se o nome do arquivo de log padrão for usado, o formulário será%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br /> O valor padrão é 0, o que significa que não há nenhum máximo. <br /> | 
| <strong>FileName</strong> | <strong>REG_SZ</strong> | Caminho totalmente qualificado do arquivo de log. O caminho para esse arquivo deve existir. O arquivo de log é um arquivo de log sequencial. Observe que todos os provedores que gravam eventos na sessão do agente global gravam eventos nesse arquivo de log. O caminho é limitado a 1024 caracteres. Se <strong>filename</strong> não for especificado, os eventos serão gravados em%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>antes do Windows Vista:</strong> O arquivo padrão é%SystemRoot%\System32\LogFiles\WMI\Trace.log.<br /><br /> | 
| <strong>FlushTimer</strong> | <strong>REG_DWORD</strong> | Com que frequência, em segundos, os buffers de rastreamento são liberados forçosamente. O tempo de liberação mínimo é de 1 segundo. Essa liberação forçada é além da liberação automática que ocorre quando um buffer está cheio e quando a sessão de rastreamento é interrompida. <br /> Para o caso de um agente em tempo real, um valor igual a zero (o valor padrão) significa que o tempo de liberação será definido como 1 segundo. Um agente de log em tempo real é quando <strong>LOGFILEMODE</strong> é definido como <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br /> O valor padrão é 0. Por padrão, os buffers são liberados somente quando estão cheios. <br /> | 
| <strong>LogFilemode</strong> | <strong>REG_DWORD</strong> | Especifica as opções de sessão de log. Para valores, consulte <a href="logging-mode-constants.md">constantes do modo de log</a>. esses valores têm suporte no Windows Vista e versões posteriores. <br /> | 
| <strong>MaximumBuffers</strong> | <strong>REG_DWORD</strong> | O número máximo de buffers a serem alocados. Normalmente, esse valor é o número mínimo de buffers, mais vinte. O ETW usa o tamanho do buffer e o tamanho da memória física para calcular esse valor. Esse valor deve ser maior ou igual ao valor de <strong>MinimumBuffers</strong>.<br /> | 
| <strong>MaxFileSize</strong> | <strong>REG_DWORD</strong> | O tamanho máximo, em megabytes, do arquivo de log de rastreamento de eventos. Por padrão, não há nenhum tamanho máximo de arquivo.<br /> | 
| <strong>MinimumBuffers</strong> | <strong>REG_DWORD</strong> | O número mínimo de buffers a serem alocados quando a sessão global do agente é iniciada. O número mínimo de buffers que você pode especificar é de dois buffers por processador. Por exemplo, em um único computador de processador, o número mínimo de buffers é dois. <br /> O valor padrão em um sistema de processador único é 0x3.<br /> | 
| <strong>Status</strong> | <strong>REG_DWORD</strong> | O status de inicialização do agente de log global. Se o agente de log global não for iniciado, o valor dessa chave será o código de erro Win32 apropriado. Se o agente global for iniciado com êxito, o valor dessa chave será ERROR_SUCCESS (0).<br /> | 




 

Depois que o registro tiver sido modificado e o computador for reiniciado, a sessão global do agente iniciará automaticamente e será usada como qualquer outra sessão com uma exceção: você usará o \_ identificador constante de ID do agente de log global do WMI \_ \_ (definido em Wmistr. h) para fazer referência à sessão global do agente. Essa constante pode ser usada como um argumento para qualquer função de rastreamento de eventos que aceite um identificador de sessão. Em funções que aceitam um nome de sessão, use o \_ nome do agente de log global \_ .

O controlador do Global Logger não chama a [**função EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar provedores. O provedor é responsável por determinar se a sessão do Global Logger foi iniciada e, em seguida, habilitando a si mesmo.

Para determinar se a sessão do Global Logger foi iniciada, você pode chamar a função [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) definindo *SessionHandle* como ID do WMI GLOBAL LOGGER e ControlCode como \_ EVENT TRACE CONTROL \_ \_ **\_ \_ \_ QUERY**.  Se a chamada **controlTrace** for bem-sucedida, a sessão do Global Logger existirá e o provedor poderá habilitar a si mesmo e registrar eventos na sessão do Global Logger (a **função ControlTrace** retornará ERROR WMI INSTANCE NOT FOUND se o Global Logger não \_ estiver \_ \_ \_ ativo).

Normalmente, o controlador é responsável por passar os sinalizadores de habilitar e o nível para o provedor quando ele habilita o provedor, mas como o controlador do Global Logger não habilita o provedor, é responsabilidade do provedor passar essas informações para ele mesmo, se necessário.

A sessão do Global Logger é um recurso limitado e deve ser usada com moderação. Os serviços que querem capturar informações durante o processo de inicialização devem considerar adicionar a lógica do controlador a si mesmo em vez de usar a sessão do Global Logger.

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão de logger privado, consulte [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do NT Kernel Logger, consulte Configurando e iniciando a [sessão do NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md).

