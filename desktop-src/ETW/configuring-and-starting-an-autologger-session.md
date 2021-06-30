---
description: A sessão de rastreamento de eventos do agente autologger registra eventos que ocorrem no início do processo de inicialização do sistema operacional.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurando e iniciando uma sessão do agente de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102035"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="cbcca-103">Configurando e iniciando uma sessão do agente de log</span><span class="sxs-lookup"><span data-stu-id="cbcca-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="cbcca-104">A sessão de rastreamento de eventos do agente autologger registra eventos que ocorrem no início do processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cbcca-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="cbcca-105">Aplicativos e drivers de dispositivo podem usar a sessão de agente de log autologger para capturar rastreamentos antes que o usuário faça logon.</span><span class="sxs-lookup"><span data-stu-id="cbcca-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="cbcca-106">Observe que alguns drivers de dispositivo, como drivers de dispositivo de disco, não são carregados no momento em que a sessão do agente de log é iniciada.</span><span class="sxs-lookup"><span data-stu-id="cbcca-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="cbcca-107">O agente de log autologger difere do agente de log global das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="cbcca-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="cbcca-108">Você pode especificar uma ou mais sessões do autologger (o agente global era uma única sessão para a qual todos os eventos registraram).</span><span class="sxs-lookup"><span data-stu-id="cbcca-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="cbcca-109">O agente de log de eventos envia uma notificação de habilitação para os provedores quando a sessão é iniciada (o agente de log global não enviou uma notificação de habilitação aos provedores, portanto, os provedores precisavam contar com outros meios para saber se a sessão global de agente foi iniciada para iniciar eventos de log).</span><span class="sxs-lookup"><span data-stu-id="cbcca-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="cbcca-110">O agente de log autologger não dá suporte a logs de eventos de agente de kernel NT (consulte o membro **EnableFlags** das [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="cbcca-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="cbcca-111">Para registrar eventos de agente do kernel NT, você deve usar o agente de log [global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="cbcca-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="cbcca-112">Para obter mais informações sobre a visualização de agente de log global, consulte [Configurando e iniciando a sessão global de agente](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="cbcca-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="cbcca-113">O ETW dá suporte ao agente de log autologger no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cbcca-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="cbcca-114">Use o [agente de log global](configuring-and-starting-the-global-logger-session.md) em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="cbcca-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="cbcca-115">Você usa o registro para configurar a sessão do agente de log autologger.</span><span class="sxs-lookup"><span data-stu-id="cbcca-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="cbcca-116">Adicione a seguinte chave do registro, se ainda não estiver presente:</span><span class="sxs-lookup"><span data-stu-id="cbcca-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="cbcca-117">Na chave **autologger** , crie uma chave para cada sessão do autologger que você deseja configurar, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="cbcca-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="cbcca-118">Para cada sessão, crie uma chave para cada provedor que você deseja habilitar para a sessão.</span><span class="sxs-lookup"><span data-stu-id="cbcca-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="cbcca-119">Use o GUID do provedor como a chave.</span><span class="sxs-lookup"><span data-stu-id="cbcca-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="cbcca-120">A tabela a seguir descreve os valores que você pode definir para cada sessão do autologger.</span><span class="sxs-lookup"><span data-stu-id="cbcca-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="cbcca-121">Você deve ter privilégios de administrador para especificar esses valores de registro.</span><span class="sxs-lookup"><span data-stu-id="cbcca-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="cbcca-122">O valor **inicial** e o **GUID** são os únicos valores necessários para iniciar a sessão do agente de log automática; todos os outros valores têm configurações padrão que serão usadas se o valor não estiver presente no registro.</span><span class="sxs-lookup"><span data-stu-id="cbcca-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="cbcca-123">Normalmente, você deve usar os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="cbcca-123">Typically, you should use the default values.</span></span> <span data-ttu-id="cbcca-124">Se você especificar um valor que o ETW não tem suporte, o ETW substituirá o valor.</span><span class="sxs-lookup"><span data-stu-id="cbcca-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbcca-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cbcca-125">Value</span></span></th>
<th><span data-ttu-id="cbcca-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbcca-126">Type</span></span></th>
<th><span data-ttu-id="cbcca-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbcca-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbcca-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="cbcca-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-130">O tamanho de cada buffer, em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="cbcca-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="cbcca-131">Deve ser menor que um megabyte.</span><span class="sxs-lookup"><span data-stu-id="cbcca-131">Should be less than one megabyte.</span></span> <span data-ttu-id="cbcca-132">O ETW usa o tamanho da memória física para calcular esse valor.</span><span class="sxs-lookup"><span data-stu-id="cbcca-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-133"><strong>Clocktype</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="cbcca-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-135">O temporizador a ser usado ao registrar em log o carimbo de data/hora para cada evento.</span><span class="sxs-lookup"><span data-stu-id="cbcca-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="cbcca-136">1 = valor do contador de desempenho (alta resolução)</span><span class="sxs-lookup"><span data-stu-id="cbcca-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="cbcca-137">2 = temporizador do sistema</span><span class="sxs-lookup"><span data-stu-id="cbcca-137">2 = System timer</span></span></li>
<li><span data-ttu-id="cbcca-138">3 = contador de ciclo de CPU</span><span class="sxs-lookup"><span data-stu-id="cbcca-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="cbcca-139">Para obter uma descrição de cada tipo de relógio, consulte o membro <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="cbcca-140">O valor padrão é 1 (valor do contador de desempenho) no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cbcca-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="cbcca-141">Antes do Windows Vista, o valor padrão é 2 (temporizador do sistema).</span><span class="sxs-lookup"><span data-stu-id="cbcca-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="cbcca-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-144">Para desabilitar a persistência em tempo real, defina esse valor como 1.</span><span class="sxs-lookup"><span data-stu-id="cbcca-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="cbcca-145">O padrão é 0 (habilitado) para sessões em tempo real.</span><span class="sxs-lookup"><span data-stu-id="cbcca-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="cbcca-146">Se a persistência em tempo real estiver habilitada, os eventos em tempo real que não foram entregues no momento em que o computador foi desligado serão persistidos.</span><span class="sxs-lookup"><span data-stu-id="cbcca-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="cbcca-147">Os eventos serão então entregues ao consumidor na próxima vez que o consumidor se conectar à sessão.</span><span class="sxs-lookup"><span data-stu-id="cbcca-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-148"><strong>Contador de filecounter</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="cbcca-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-150">Não defina nem modifique esse valor.</span><span class="sxs-lookup"><span data-stu-id="cbcca-150">Do not set or modify this value.</span></span> <span data-ttu-id="cbcca-151">Esse valor é o número de série usado para incrementar o nome do arquivo de log se <strong>FileMax</strong> for especificado.</span><span class="sxs-lookup"><span data-stu-id="cbcca-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="cbcca-152">Se o valor não for válido, 1 será assumido.</span><span class="sxs-lookup"><span data-stu-id="cbcca-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="cbcca-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="cbcca-155">O caminho totalmente qualificado do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="cbcca-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="cbcca-156">O caminho para esse arquivo deve existir.</span><span class="sxs-lookup"><span data-stu-id="cbcca-156">The path to this file must exist.</span></span> <span data-ttu-id="cbcca-157">O arquivo de log é um arquivo de log sequencial.</span><span class="sxs-lookup"><span data-stu-id="cbcca-157">The log file is a sequential log file.</span></span> <span data-ttu-id="cbcca-158">O caminho é limitado a 1024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cbcca-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="cbcca-159">Se <strong>filename</strong> não for especificado, os eventos serão gravados em%SystemRoot%\System32\LogFiles\WMI \& lt; SessionName &gt; . etl.</span><span class="sxs-lookup"><span data-stu-id="cbcca-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="cbcca-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-162">O número máximo de instâncias do arquivo de log que o ETW cria.</span><span class="sxs-lookup"><span data-stu-id="cbcca-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="cbcca-163">Se o arquivo de log especificado em <strong>filename</strong> existir, o ETW acrescentará o valor <strong>filecounterer</strong> ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cbcca-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="cbcca-164">Por exemplo, se o nome do arquivo de log padrão for usado, o formulário será%SystemRoot%\System32\LogFiles\WMI \& lt; SessionName &gt; . etl. NNNN.</span><span class="sxs-lookup"><span data-stu-id="cbcca-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.NNNN.</span></span> <br/> <span data-ttu-id="cbcca-165">Na primeira vez que o computador é iniciado, o nome do arquivo é &lt; SessionName &gt; . etl. 0001, a segunda vez que o nome do arquivo é &lt; SessionName &gt; . etl. 0002 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbcca-165">The first time the computer is started, the file name is &lt;sessionname&gt;.etl.0001, the second time the file name is &lt;sessionname&gt;.etl.0002, and so on.</span></span> <span data-ttu-id="cbcca-166">Se <strong>FileMax</strong> for 3, na quarta reinicialização do computador, o ETW redefinirá o contador como 1 e substituirá &lt; SessionName &gt; . etl. 0001, se existir.</span><span class="sxs-lookup"><span data-stu-id="cbcca-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites &lt;sessionname&gt;.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="cbcca-167">O número máximo de instâncias do arquivo de log com suporte é 16.</span><span class="sxs-lookup"><span data-stu-id="cbcca-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="cbcca-168">Não use esse recurso com o modo de arquivo de log <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="cbcca-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-171">Com que frequência, em segundos, os buffers de rastreamento são liberados forçosamente.</span><span class="sxs-lookup"><span data-stu-id="cbcca-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="cbcca-172">O tempo de liberação mínimo é de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="cbcca-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="cbcca-173">Essa liberação forçada é além da liberação automática que ocorre quando um buffer está cheio e quando a sessão de rastreamento é interrompida.</span><span class="sxs-lookup"><span data-stu-id="cbcca-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="cbcca-174">Para o caso de um agente em tempo real, um valor igual a zero (o valor padrão) significa que o tempo de liberação será definido como 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="cbcca-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="cbcca-175">Um agente de log em tempo real é quando <strong>LOGFILEMODE</strong> é definido como <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="cbcca-176">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="cbcca-176">The default value is 0.</span></span> <span data-ttu-id="cbcca-177">Por padrão, os buffers são liberados somente quando estão cheios.</span><span class="sxs-lookup"><span data-stu-id="cbcca-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-178"><strong>Volume</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="cbcca-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="cbcca-180">Uma cadeia de caracteres que contém um GUID que identifica exclusivamente a sessão.</span><span class="sxs-lookup"><span data-stu-id="cbcca-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="cbcca-181">Esse valor é necessário.</span><span class="sxs-lookup"><span data-stu-id="cbcca-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-182"><strong>LogFilemode</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="cbcca-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-184">Especifique um ou mais modos de log.</span><span class="sxs-lookup"><span data-stu-id="cbcca-184">Specify one or more log modes.</span></span> <span data-ttu-id="cbcca-185">Para obter os valores possíveis, consulte <a href="logging-mode-constants.md">constantes do modo de log</a>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="cbcca-186">O padrão é <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="cbcca-187">Em vez de gravar em um arquivo de log, você pode especificar <strong>EVENT_TRACE_BUFFERING_MODE</strong> ou <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="cbcca-188">A especificação de <strong>EVENT_TRACE_BUFFERING_MODE</strong> evita o custo de liberação do conteúdo da sessão para o disco quando o sistema de arquivos fica disponível.</span><span class="sxs-lookup"><span data-stu-id="cbcca-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="cbcca-189">Observe que o uso de <strong>EVENT_TRACE_BUFFERING_MODE</strong> fará com que o sistema ignore o valor <strong>MaximumBuffers</strong> , pois o tamanho do buffer é, em vez disso, o produto de <strong>MinimumBuffers</strong> e <strong>BufferSize</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="cbcca-190">As sessões do autologger não dão suporte ao modo de log de <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="cbcca-191">Se <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> for especificado, <strong>BufferSize</strong> deverá ser fornecido explicitamente e deverá ser o mesmo no agente de log e no arquivo que está sendo anexado.</span><span class="sxs-lookup"><span data-stu-id="cbcca-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="cbcca-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-194">O tamanho máximo do arquivo de log, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="cbcca-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="cbcca-195">A sessão é fechada quando o tamanho máximo é atingido, a menos que você esteja no modo de arquivo de log circular.</span><span class="sxs-lookup"><span data-stu-id="cbcca-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="cbcca-196">Para especificar sem limite, defina valor como 0.</span><span class="sxs-lookup"><span data-stu-id="cbcca-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="cbcca-197">O padrão é 100 MB, se não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="cbcca-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="cbcca-198">O comportamento que ocorre quando o tamanho máximo do arquivo é atingido depende do valor de <strong>LOGFILEMODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="cbcca-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-201">O número máximo de buffers a serem alocados.</span><span class="sxs-lookup"><span data-stu-id="cbcca-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="cbcca-202">Normalmente, esse valor é o número mínimo de buffers, mais vinte.</span><span class="sxs-lookup"><span data-stu-id="cbcca-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="cbcca-203">O ETW usa o tamanho do buffer e o tamanho da memória física para calcular esse valor.</span><span class="sxs-lookup"><span data-stu-id="cbcca-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="cbcca-204">Esse valor deve ser maior ou igual ao valor de <strong>MinimumBuffers</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="cbcca-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-207">O número mínimo de buffers a serem alocados na inicialização.</span><span class="sxs-lookup"><span data-stu-id="cbcca-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="cbcca-208">O número mínimo de buffers que você pode especificar é de dois buffers por processador.</span><span class="sxs-lookup"><span data-stu-id="cbcca-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="cbcca-209">Por exemplo, em um único computador de processador, o número mínimo de buffers é dois.</span><span class="sxs-lookup"><span data-stu-id="cbcca-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-210"><strong>Iniciar</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="cbcca-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-212">Para que a sessão do autologger seja iniciada na próxima vez que o computador for reiniciado, defina esse valor como 1; caso contrário, defina esse valor como 0.</span><span class="sxs-lookup"><span data-stu-id="cbcca-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-213"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="cbcca-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-215">O status de inicialização do agente de log autologger.</span><span class="sxs-lookup"><span data-stu-id="cbcca-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="cbcca-216">Se o agente de log automática não for iniciado, o valor dessa chave será o código de erro Win32 apropriado.</span><span class="sxs-lookup"><span data-stu-id="cbcca-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="cbcca-217">Se o agente de log autologger foi iniciado com êxito, o valor dessa chave será <strong>ERROR_SUCCESS</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="cbcca-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cbcca-218">A tabela a seguir descreve os valores que você pode definir para cada provedor que você deseja habilitar na sua sessão.</span><span class="sxs-lookup"><span data-stu-id="cbcca-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="cbcca-219">Você deve ter privilégios de administrador para especificar esses valores de registro.</span><span class="sxs-lookup"><span data-stu-id="cbcca-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="cbcca-220">Se você especificar um valor que o ETW não tem suporte, o ETW substituirá o valor.</span><span class="sxs-lookup"><span data-stu-id="cbcca-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbcca-221">Valor</span><span class="sxs-lookup"><span data-stu-id="cbcca-221">Value</span></span></th>
<th><span data-ttu-id="cbcca-222">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbcca-222">Type</span></span></th>
<th><span data-ttu-id="cbcca-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbcca-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbcca-224"><strong>Enabled</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="cbcca-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-226">Determina se o provedor está habilitado.</span><span class="sxs-lookup"><span data-stu-id="cbcca-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="cbcca-227">Para habilitar o provedor, defina esse valor como 1.</span><span class="sxs-lookup"><span data-stu-id="cbcca-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="cbcca-228">Para desabilitar o provedor, defina esse valor como 0.</span><span class="sxs-lookup"><span data-stu-id="cbcca-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="cbcca-229">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="cbcca-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="cbcca-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-232">Valor definido pelo provedor que especifica a classe de eventos para os quais o provedor gera eventos.</span><span class="sxs-lookup"><span data-stu-id="cbcca-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="cbcca-233">Para obter detalhes, consulte o parâmetro <em>EnableFlags</em> da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="cbcca-234">Especifique esse nome de valor se o provedor não oferecer suporte a <strong>MatchAnyKeyword</strong> ou <strong>MatchAllKeyword</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="cbcca-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-237">Valor definido pelo provedor que especifica o nível de detalhe incluído no evento.</span><span class="sxs-lookup"><span data-stu-id="cbcca-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="cbcca-238">Por exemplo, você pode usar esse valor para indicar o nível de severidade dos eventos (informativo, aviso, erro) que o provedor gera.</span><span class="sxs-lookup"><span data-stu-id="cbcca-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="cbcca-239">Para obter uma lista de níveis predefinidos, consulte o parâmetro <em>Level</em> da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-240"><strong>Habilitada</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="cbcca-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-242">Use esse valor para incluir um ou mais dos seguintes itens no arquivo de log:</span><span class="sxs-lookup"><span data-stu-id="cbcca-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="cbcca-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = incluir nos dados estendidos o Sid (identificador de segurança) do usuário.</span><span class="sxs-lookup"><span data-stu-id="cbcca-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="cbcca-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = incluir nos dados estendidos o identificador de sessão de terminal.</span><span class="sxs-lookup"><span data-stu-id="cbcca-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="cbcca-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = incluir nos dados estendidos um rastreamento de pilha de chamadas para eventos escritos usando <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cbcca-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="cbcca-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra todos os eventos que não têm uma palavra-chave diferente de zero especificada.</span><span class="sxs-lookup"><span data-stu-id="cbcca-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="cbcca-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica que essa chamada para <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> deve habilitar um <a href="provider-traits.md">grupo de provedores</a> em vez de um provedor de eventos individual.</span><span class="sxs-lookup"><span data-stu-id="cbcca-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="cbcca-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = incluir a chave de início do processo nos dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="cbcca-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="cbcca-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = incluir a chave de evento nos dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="cbcca-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="cbcca-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtra todos os eventos que estão marcados como um evento InPrivate ou que vêm de um processo marcado como InPrivate.</span><span class="sxs-lookup"><span data-stu-id="cbcca-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="cbcca-251">Para obter mais informações sobre esses itens, consulte a <strong>habilitação</strong> da estrutura de <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbcca-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="cbcca-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-254">Bitmask de palavras-chave que determinam a categoria de eventos que você deseja que o provedor escreva.</span><span class="sxs-lookup"><span data-stu-id="cbcca-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="cbcca-255">O provedor gravará o evento se qualquer um dos bits de palavra-chave do evento corresponder a qualquer um dos bits definidos nessa máscara.</span><span class="sxs-lookup"><span data-stu-id="cbcca-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="cbcca-256">Para especificar que o provedor grava todos os eventos, defina esse valor como zero.</span><span class="sxs-lookup"><span data-stu-id="cbcca-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="cbcca-257">Para obter um exemplo, consulte a seção comentários da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbcca-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="cbcca-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="cbcca-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="cbcca-260">Esse bitmask é opcional.</span><span class="sxs-lookup"><span data-stu-id="cbcca-260">This bitmask is optional.</span></span> <span data-ttu-id="cbcca-261">Essa máscara restringe ainda mais a categoria de eventos que você deseja que o provedor escreva.</span><span class="sxs-lookup"><span data-stu-id="cbcca-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="cbcca-262">Se a palavra-chave do evento atender à condição <em>MatchAnyKeyword</em> , o provedor gravará o evento somente se todos os bits nessa máscara existirem na palavra-chave do evento.</span><span class="sxs-lookup"><span data-stu-id="cbcca-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="cbcca-263">Essa máscara não será usada se <em>MatchAnyKeyword</em> for zero.</span><span class="sxs-lookup"><span data-stu-id="cbcca-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="cbcca-264">Para obter um exemplo, consulte a seção comentários da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cbcca-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cbcca-265">Depois que o registro tiver sido modificado, a sessão do agente de log automática será iniciada na próxima vez em que o computador for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="cbcca-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="cbcca-266">A sessão do autologger chama a função [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar os provedores.</span><span class="sxs-lookup"><span data-stu-id="cbcca-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="cbcca-267">As sessões do autologger aumentam o tempo de inicialização do sistema e devem ser usadas com moderação.</span><span class="sxs-lookup"><span data-stu-id="cbcca-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="cbcca-268">Os serviços que desejam capturar informações durante o processo de inicialização devem considerar a adição da lógica do controlador a si só, em vez de usar a sessão do agente de log.</span><span class="sxs-lookup"><span data-stu-id="cbcca-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="cbcca-269">Para interromper uma sessão do agente de log, chame a função [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) .</span><span class="sxs-lookup"><span data-stu-id="cbcca-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="cbcca-270">O nome da sessão que você passa para a função é o nome da chave do registro que você usou para definir a sessão no registro.</span><span class="sxs-lookup"><span data-stu-id="cbcca-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="cbcca-271">No Windows 8.1, o Windows Server 2012 R2 e posterior, o conteúdo do evento, o escopo e os filtros de exame de pilha podem ser usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e pelas estruturas [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descritor de filtro de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar as condições específicas em uma sessão de agente.</span><span class="sxs-lookup"><span data-stu-id="cbcca-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="cbcca-272">Para obter mais informações sobre filtros de carga de evento, consulte as funções [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e as estruturas [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **Enable \_ trace \_**, **\_ \_ descritor de filtro de evento** e conteúdo de filtro de carga.</span><span class="sxs-lookup"><span data-stu-id="cbcca-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="cbcca-273">Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="cbcca-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="cbcca-274">Para obter detalhes sobre como iniciar uma sessão de agente de log particular, consulte [Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="cbcca-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="cbcca-275">Para obter detalhes sobre como iniciar uma sessão do agente do NT kernel, consulte [Configurando e iniciando a sessão do agente de log do NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="cbcca-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbcca-276">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbcca-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbcca-277">Configurando e iniciando uma sessão de agente de log particular</span><span class="sxs-lookup"><span data-stu-id="cbcca-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="cbcca-278">Configurando e iniciando uma sessão SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="cbcca-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="cbcca-279">Configurando e iniciando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="cbcca-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="cbcca-280">Configurando e iniciando a sessão do NT kernel logger</span><span class="sxs-lookup"><span data-stu-id="cbcca-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="cbcca-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="cbcca-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="cbcca-282">**Habilitar \_ parâmetros de rastreamento \_**</span><span class="sxs-lookup"><span data-stu-id="cbcca-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="cbcca-283">**\_descritor de filtro de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="cbcca-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="cbcca-284">**predicado de filtro de carga \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cbcca-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="cbcca-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="cbcca-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="cbcca-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="cbcca-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="cbcca-287">Atualizando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="cbcca-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
