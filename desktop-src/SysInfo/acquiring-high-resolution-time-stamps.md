---
description: O Windows fornece APIs que você pode usar para adquirir carimbos de data/hora de alta resolução ou intervalos de tempo de medida.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Aquisição de carimbos de data/hora de alta resolução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922978"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Aquisição de carimbos de data/hora de alta resolução

O Windows fornece APIs que você pode usar para adquirir carimbos de data/hora de alta resolução ou intervalos de tempo de medida. A API principal para código nativo é [**QueryPerformanceCounter (Qpc)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Para drivers de dispositivo, a API do modo kernel é [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Para código gerenciado, a classe [**System. Diagnostics. cronômetro**](/previous-versions/windows/) usa **QPC** como sua base de tempo exata.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é independente de e não é sincronizado com nenhuma referência de hora externa. Para recuperar carimbos de data/hora que podem ser sincronizados com uma referência de hora externa, como o UTC (tempo Universal Coordenado) para uso em medidas de tempo de alta resolução, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

Carimbos de data/hora e medições de intervalo de tempo são parte integrante de medidas de desempenho de computador e rede. Essas operações de medição de desempenho incluem a computação do tempo de resposta, a taxa de transferência e a latência, bem como a execução do código de criação de perfil. Cada uma dessas operações envolve uma medida de atividades que ocorrem durante um intervalo de tempo que é definido por um evento de início e de término que pode ser independente de qualquer referência de horário de dia externa.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) normalmente é o melhor método a ser usado para eventos de carimbo de data/hora e medir pequenos intervalos de tempo que ocorrem no mesmo sistema ou máquina virtual. Considere o uso de [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) quando você quiser eventos de carimbo de data/hora em vários computadores, desde que cada computador esteja participando de um esquema de sincronização de tempo, como o protocolo NTP (NTP). O **QPC** ajuda a evitar dificuldades que podem ser encontradas com outras abordagens de medição de tempo, como a leitura direta do TSC (contador de carimbo de data/hora) do processador.

-   [Suporte do QPC em versões do Windows](#qpc-support-in-windows-versions)
-   [Diretrizes para aquisição de carimbos de data/hora](#guidance-for-acquiring-time-stamps)
    -   [Virtualização](#virtualization)
    -   [Uso direto de TSC](#direct-tsc-usage)
    -   [Exemplos para aquisição de carimbos de data/hora](#examples-for-acquiring-time-stamps)
-   [Perguntas frequentes gerais sobre QPC e TSC](#general-faq-about-qpc-and-tsc)
-   [Perguntas frequentes sobre programação com QPC e TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Características do relógio de hardware de nível baixo](#low-level-hardware-clock-characteristics)
    -   [Relógios absolutos e relógios de diferença](#absolute-clocks-and-difference-clocks)
    -   [Resolução, precisão, precisão e estabilidade](#resolution-precision-accuracy-and-stability)
-   [Informações do timer de hardware](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Suporte do QPC em versões do Windows

O [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) foi introduzido no Windows 2000 e no Windows XP e evoluiu para aproveitar os aprimoramentos na plataforma e nos processadores de hardware. Aqui, descrevemos as características do **QPC** em diferentes versões do Windows para ajudá-lo a manter o software executado nessas versões do Windows.

### <a name="windows-xp-and-windows-2000"></a>Windows XP e Windows 2000

O [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) está disponível no Windows XP e no Windows 2000 e funciona bem na maioria dos sistemas. No entanto, o BIOS de alguns sistemas de hardware não indicava corretamente as características de CPU de hardware (um TSC não invariável) e alguns sistemas com vários núcleos ou multiprocessadores usaram processadores com TSCs que não podiam ser sincronizados em núcleos. Sistemas com firmware com falhas que executam essas versões do Windows podem não fornecer a mesma leitura de **QPC** em núcleos diferentes se usaram o TSC como a base para **QPC**.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista e Windows Server 2008

Todos os computadores fornecidos com o Windows Vista e o Windows Server 2008 usavam um contador de plataforma (HPET) ou o temporizador de gerenciamento de energia (temporizador PM) da ACPI como a base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Esses temporizadores de plataforma têm latência de acesso maior do que o TSC e são compartilhados entre vários processadores. Isso limita a escalabilidade de **QPC** se ele for chamado simultaneamente de vários processadores.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

A maioria dos computadores com Windows 7 e Windows Server 2008 R2 tem processadores com TSCs de taxa constante e usa esses contadores como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). TSCs são contadores de hardware de alta resolução por processador que podem ser acessados com baixa latência e sobrecarga (na ordem de 10s ou centenas de ciclos de máquina, dependendo do tipo de processador). O Windows 7 e o Windows Server 2008 R2 usam o TSCs como a base do **QPC** em sistemas de domínio de relógio único em que o sistema operacional (ou o hipervisor) é capaz de sincronizar rigidamente o TSCs individual em todos os processadores durante a inicialização do sistema. Nesses sistemas, o custo de leitura do contador de desempenho é significativamente menor em comparação com os sistemas que usam um contador de plataforma. Além disso, não há nenhuma sobrecarga adicional para chamadas simultâneas e as consultas de modo de usuário, muitas vezes, ignoram as chamadas do sistema, o que reduz ainda mais a sobrecarga. Em sistemas em que o TSC não é adequado para o tempo de manutenção, o Windows seleciona automaticamente um contador de plataforma (o temporizador HPET ou o temporizador ACPI PM) como a base para **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2

O Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 usam o TSCs como base para o contador de desempenho. O algoritmo de sincronização de TSC foi significativamente melhorado para acomodar melhor sistemas grandes com muitos processadores. Além disso, o suporte para a nova API de hora do dia precisa foi adicionada, o que permite a aquisição de carimbos de hora de relógio de parede precisos do sistema operacional. Para obter mais informações, consulte [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Em plataformas de PC Windows RT, o contador de desempenho se baseia em um contador de plataforma proprietário ou no contador de sistema fornecido pelo temporizador genérico do PC com Windows RT se a plataforma estiver tão equipada.

## <a name="guidance-for-acquiring-time-stamps"></a>Diretrizes para aquisição de carimbos de data/hora

O Windows tem e continuará a investir no fornecimento de um contador de desempenho confiável e eficiente. Quando você precisar de carimbos de data/hora com uma resolução de 1 microssegundo ou melhor e não precisar que os carimbos de data/hora sejam sincronizados com uma referência de hora externa, escolha [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)ou [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise). Quando precisar de carimbos de data/hora sincronizados por UTC com uma resolução de 1 microssegundo ou melhor, escolha [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) ou [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

Em um número relativamente pequeno de plataformas que não podem usar o registro de TSC como a base [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , por exemplo, por motivos explicados em [informações de temporizador de hardware](#hardware-timer-info), a aquisição de carimbos de data/hora de alta resolução pode ser significativamente mais cara do que a aquisição de carimbos de data/hora com menor resolução. Se a resolução de 10 a 16 milissegundos for suficiente, você poderá usar [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)ou [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) para obter carimbos de data/hora que não são sincronizados com uma referência de hora externa. Para carimbos de data/hora sincronizados por UTC, use [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) ou [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Se for necessária uma resolução mais alta, você poderá usar [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)ou [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) para obter carimbos de hora em vez disso.

Em geral, os resultados do contador de desempenho são consistentes em todos os processadores em sistemas com vários núcleos e vários processadores, mesmo quando medidos em threads ou processos diferentes. Aqui estão algumas exceções a essa regra:

-   Sistemas operacionais anteriores ao Windows Vista que são executados em determinados processadores podem violar essa consistência devido a um destes motivos:

    -   Os processadores de hardware têm um TSC não invariável e o BIOS não indica essa condição corretamente.
    -   O algoritmo de sincronização de TSC que foi usado não era adequado para sistemas com um grande número de processadores.

-   Quando você compara os resultados do contador de desempenho que são adquiridos de threads diferentes, considere os valores que diferem em ± 1 Tick para que tenham uma ordenação ambígua. Se os carimbos de data/hora forem tirados do mesmo thread, essa incerteza de ± 1 Tick não se aplicará. Nesse contexto, o termo Tick refere-se a um período de tempo igual a 1 ÷ (a frequência do contador de desempenho obtido de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).

Quando você usa o contador de desempenho em sistemas de servidor grandes com domínios de vários relógios que não são sincronizados no hardware, o Windows determina que o TSC não pode ser usado para fins de tempo e seleciona um contador de plataforma como a base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Embora esse cenário ainda gere carimbos de data/hora confiáveis, a latência de acesso e a escalabilidade são afetadas negativamente. Portanto, como mencionado anteriormente nas diretrizes de uso anteriores, use apenas as APIs que fornecem uma resolução de 1 microssegundo ou melhor quando essa resolução é necessária. O TSC é usado como base para **QPC** em sistemas de domínio de vários relógios que incluem a sincronização de hardware de todos os domínios de relógio do processador, pois isso efetivamente os torna como um sistema de domínio de relógio único.

A frequência do contador de desempenho é fixa na inicialização do sistema e é consistente em todos os processadores, de modo que você só precisa consultar a frequência de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) à medida que o aplicativo é inicializado e, em seguida, armazenar em cache o resultado.

### <a name="virtualization"></a>Virtualização

O contador de desempenho deve funcionar de forma confiável em todas as máquinas virtuais convidadas em execução em hipervisores implementados corretamente. No entanto, os hipervisores que estão em conformidade com a interface do hipervisor versão 1,0 e a superfície do esclarecimento do tempo de referência podem oferecer sobrecarga substancialmente menor. Para obter mais informações sobre interfaces e esclarecimentos do hipervisor, consulte [especificações do hipervisor](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Uso direto de TSC

É altamente recomendável usar a instrução de processador **RDTSC** ou **RDTSCP** para consultar o TSC diretamente, pois você não obterá resultados confiáveis em algumas versões do Windows, em migrações ao vivo de máquinas virtuais e em sistemas de hardware sem invariável ou sincronizado com TSCs. Em vez disso, incentivamos você a usar o [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para aproveitar a abstração, a consistência e a portabilidade que ele oferece.

### <a name="examples-for-acquiring-time-stamps"></a>Exemplos para aquisição de carimbos de data/hora

Os vários exemplos de código nessas seções mostram como adquirir carimbos de data/hora.

### <a name="using-qpc-in-native-code"></a>Usando QPC em código nativo

Este exemplo mostra como usar [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) em código nativo C e C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Adquirindo carimbos de data/hora de alta resolução do código gerenciado

Este exemplo mostra como usar a classe [**System. Diagnostics. cronômetro**](/previous-versions/windows/) de código gerenciado.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



A classe [**System. Diagnostics. cronômetro**](/previous-versions/windows/) também fornece vários métodos convenientes para executar medições de intervalo de tempo.

### <a name="using-qpc-from-kernel-mode"></a>Usando QPC do modo kernel

O kernel do Windows fornece acesso de modo kernel ao contador de desempenho por meio de [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) do qual o contador de desempenho e a frequência de desempenho podem ser obtidos. O **KeQueryPerformanceCounter** está disponível apenas no modo kernel e é fornecido para gravadores de drivers de dispositivo e outros componentes do modo kernel.

Este exemplo mostra como usar [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) no modo de kernel C e C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>Perguntas frequentes gerais sobre QPC e TSC

Aqui estão as respostas para perguntas frequentes sobre [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e TSCs em geral.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**É QueryPerformanceCounter () o mesmo que a função Win32 Get () ou GetTickCount64 ()?**
</dt> <dd>

Não. O [**ObterContagemMarcaEscala**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) e o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) não estão relacionados a [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). O **ObterContagemMarcaEscala** e o **GetTickCount64** retornam o número de milissegundos desde que o sistema foi iniciado.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**Devo usar o QPC ou chamar as instruções do RDTSC/RDTSCP diretamente?**
</dt> <dd>

Para evitar problemas de incorreção e portabilidade, é altamente recomendável usar [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) em vez de usar o registro de TSC ou as instruções do processador **RDTSC** ou **RDTSCP** .

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Qual é a relação de QPC com uma época de tempo externa? Ele pode ser sincronizado com uma época externa, como UTC?**
</dt> <dd>

O [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é baseado em um contador de hardware que não pode ser sincronizado com uma referência de hora externa, como o UTC. Para carimbos de data/hora precisos que podem ser sincronizados com uma referência UTC externa, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**O QPC é afetado pelo horário de verão, segundos bissextos, fusos horários ou alterações de hora do sistema feitas pelo administrador?**
</dt> <dd>

Não. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é completamente independente da hora do sistema e UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**A precisão do QPC é afetada pelas alterações de frequência do processador causadas pela tecnologia de gerenciamento de energia ou Turbo Boost?**
</dt> <dd>

Não. Se o processador tiver um TSC invariável, o [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) não será afetado por esses tipos de alterações. Se o processador não tiver um TSC invariável, o **QPC** será revertido para um temporizador de hardware de plataforma que não será afetado pelas alterações de frequência do processador ou pela tecnologia Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**O QPC funciona de forma confiável em sistemas com vários processadores, sistemas com vários núcleos e sistema com o hyperthreading?**
</dt> <dd>

Yes

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Como fazer determinar e validar que o QPC funciona em meu computador?**
</dt> <dd>

Você não precisa executar essas verificações.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Quais processadores têm TSCs não invariáveis? Como posso verificar se meu sistema tem um TSC não invariável?**
</dt> <dd>

Você não precisa executar essa verificação por conta própria. Os sistemas operacionais Windows executam várias verificações na inicialização do sistema para determinar se o TSC é adequado como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). No entanto, para fins de referência, você pode determinar se o processador tem um TSC invariável usando um destes:

-   o utilitário Coreinfo.exe do Windows Sysinternals
-   verificando os valores retornados pela instrução CPUID referente às características de TSC
-   a documentação do fabricante do processador

O seguinte mostra as informações de TSC-invariáveis fornecidas pelo utilitário Windows Sysinternals Coreinfo.exe ([www.sysInternals.com](https://www.sysinternals.com)). Um asterisco significa "verdadeiro".

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**O QPC funciona de maneira confiável em plataformas de hardware de PC com Windows RT?**
</dt> <dd>

Yes

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Com que frequência o QPC se sobreverte?**
</dt> <dd>

Não menos de 100 anos a partir da inicialização mais recente do sistema e possivelmente mais com base no temporizador de hardware subjacente usado. Para a maioria dos aplicativos, a sobreposição não é uma preocupação.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Qual é o custo computacional de chamar QPC?**
</dt> <dd>

O custo de chamada computacional do [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é determinado principalmente pela plataforma de hardware subjacente. Se o registro de TSC for usado como base para QPC, o custo computacional será determinado principalmente pelo tempo que o processador leva para processar uma instrução **RDTSC** . Esse tempo varia de 10s de ciclos de CPU a várias centenas de ciclos de CPU, dependendo do processador usado. Se o TSC não puder ser usado, o sistema selecionará uma base de tempo de hardware diferente. Como essas bases de tempo estão localizadas na placa-mãe (por exemplo, na ponte de sul da PCI ou PCH), o custo computacional por chamada é maior do que o TSC e está frequentemente na vizinhança de 0,8 a 1,0 microssegundos, dependendo da velocidade do processador e de outros fatores de hardware. Esse custo é dominado pelo tempo necessário para acessar o dispositivo de hardware na placa-mãe.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**O QPC requer uma transição de kernel (chamada do sistema)?**
</dt> <dd>

Uma transição de kernel não será necessária se o sistema puder usar o registro TSC como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Se o sistema precisar usar uma base de tempo diferente, como o temporizador HPET ou PM, será necessária uma chamada do sistema.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**O contador de desempenho é monotônico (sem redução)?**
</dt> <dd>

Yes

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**O contador de desempenho pode ser usado para ordenar eventos no tempo?**
</dt> <dd>

Sim. No entanto, ao comparar os resultados do contador de desempenho que são adquiridos de threads diferentes, os valores que diferem em ± 1 Tick têm uma ordenação ambígua como se tivessem um carimbo de data/hora idêntico.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Quão precisa é o contador de desempenho?**
</dt> <dd>

A resposta depende de uma variedade de fatores. Para obter mais informações, consulte [características de relógio de hardware de baixo nível](#low-level-hardware-clock-characteristics).

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Perguntas frequentes sobre programação com QPC e TSC

Aqui estão as respostas para perguntas frequentes sobre programação com [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e TSCs.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Preciso converter a saída do QPC em milissegundos. Como posso evitar a perda de precisão com a conversão em Double ou float?**
</dt> <dd>

Há várias coisas a ter em mente ao executar cálculos em contadores de desempenho de inteiros:

-   A divisão de inteiro perderá o resto. Isso pode causar perda de precisão em alguns casos.
-   A conversão entre os inteiros de 64 bits e o ponto flutuante (duplo) pode causar perda de precisão porque o ponto flutuante mantissa não pode representar todos os valores integrais possíveis.
-   A multiplicação de inteiros de 64 bits pode resultar em estouro de inteiro.

Como princípio geral, adie esses cálculos e conversões o mais longo possível para evitar a composição dos erros introduzidos.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Como posso converter QPC em tiques de 100 nanossegundos para que eu possa adicioná-lo a um FILETIME?**
</dt> <dd>

Uma hora do arquivo é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos decorridos desde as 12:00 A.M. 1º de janeiro de 1601 UTC (tempo Universal Coordenado). Os horários de arquivo são usados pelas chamadas à API do Win32 que retornam a hora do dia, como [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) e [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Por outro lado, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) retorna valores que representam o tempo em unidades de 1/(a frequência do contador de desempenho obtido de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)). A conversão entre os dois exige o cálculo da taxa dos intervalos de intervalo de **QPC** e 100-nanossegundos. Tenha cuidado para evitar a perda de precisão porque os valores podem ser pequenos (0, 1/0, 340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Por que o carimbo de data/hora que é retornado de QPC um inteiro assinado?**
</dt> <dd>

Cálculos que envolvem carimbos de data/hora [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) podem envolver subtração. Usando um valor assinado, você pode manipular cálculos que podem gerar valores negativos.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Como posso obter carimbos de data/hora de alta resolução do código gerenciado?**
</dt> <dd>

Chame o método [**cronômetro. GetTimestamp**](/previous-versions/windows/) da classe [**System. Diagnostics. cronômetro**](/previous-versions/windows/) . Para obter um exemplo de como usar o **cronômetro. GetTimestamp**, consulte [adquirindo carimbos de data/hora de alta resolução do código gerenciado](#acquiring-high-resolution-time-stamps-from-managed-code).

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**Em que circunstâncias QueryPerformanceFrequency retorna FALSE ou QueryPerformanceCounter retorna zero?**
</dt> <dd>

Isso não ocorrerá em nenhum sistema que execute o Windows XP ou posterior.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**Preciso definir a afinidade de thread para um único núcleo para usar o QPC?**
</dt> <dd>

Não. Para obter mais informações, consulte [diretrizes para adquirir carimbos de data/hora](#guidance-for-acquiring-time-stamps). Esse cenário não é necessário nem desejável. A execução desse cenário pode afetar negativamente o desempenho do aplicativo, restringindo o processamento a um núcleo ou criando um afunilamento em um único núcleo se vários threads definirem sua afinidade com o mesmo núcleo ao chamar [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Características do relógio de hardware de nível baixo

Essas seções mostram características de clock de hardware de baixo nível.

### <a name="absolute-clocks-and-difference-clocks"></a>Relógios absolutos e relógios de diferença

Os relógios absolutos fornecem leituras precisas do dia. Normalmente, eles são baseados em UTC (tempo Universal Coordenado) e, consequentemente, sua precisão depende em parte do quão bem eles são sincronizados com uma referência de hora externa. Os relógios de diferença medem os intervalos de tempo e normalmente não são baseados em uma época de tempo externa. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é um relógio de diferença e não é sincronizado com uma época de tempo ou referência externa. Quando você usa o **QPC** para medições de intervalo de tempo, normalmente obtém maior precisão do que seria obtido usando carimbos de data/hora que são derivados de um relógio absoluto. Isso ocorre porque o processo de sincronização do tempo de um relógio absoluto pode introduzir turnos de fase e frequência que aumentam a incerteza de medidas de intervalo de tempo de curto prazo.

### <a name="resolution-precision-accuracy-and-stability"></a>Resolução, precisão, precisão e estabilidade

O [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa um contador de hardware como base. Os timers de hardware consistem em três partes: um gerador de tiques, um contador que conta as tiques e um meio de recuperar o valor do contador. As características desses três componentes determinam a resolução, a precisão, a precisão e a estabilidade do **QPC**.

Se um gerador de hardware fornecer tiques a uma taxa constante, os intervalos de tempo podem ser medidos simplesmente contando esses tiques. A taxa na qual as tiques são geradas é chamada de frequência e expressa em Hertz (Hz). O recíproco da frequência é chamado de período ou intervalo de tiques e é expresso em uma unidade de tempo do SI (sistema internacional de unidades) apropriada (por exemplo, segundo, milissegundo, microssegundo ou nanossegundo).

![intervalo de tempo](images/tick-interval.png)

A resolução do temporizador é igual ao período. A resolução determina a capacidade de distinguir entre dois carimbos de data e hora e coloca um limite inferior nos menores intervalos de tempo que podem ser medidos. Às vezes, isso é chamado de resolução de tiques.

A medição de tempo digital introduz uma incerteza de medidas de ± 1 Tick porque o contador digital avança em etapas discretas, enquanto o tempo avança continuamente. Essa incerteza é chamada de erro de quantificação. Para medidas típicas de intervalo de tempo, esse efeito geralmente pode ser ignorado porque o erro de quantificação é muito menor do que o intervalo de tempo que está sendo medido.

![medição de tempo digital](images/digital-time-measure.png)

No entanto, se o período que está sendo medido for pequeno e se aproximar da resolução do temporizador, você precisará considerar esse erro de quantização. O tamanho do erro introduzido é aquele de um período de relógio.

Os dois diagramas a seguir ilustram o impacto da incerteza de ± 1 em escala usando um temporizador com uma resolução de 1 unidade de tempo.

![incerteza de tique](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) retorna a frequência de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), e o período e a resolução são iguais ao recíproco desse valor. A frequência do contador de desempenho que o **QueryPerformanceFrequency** retorna é determinada durante a inicialização do sistema e não é alterada enquanto o sistema está em execução.

> [!Note]  
> Podem existir casos em que [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) não retorna a frequência real do gerador de tiques de hardware. Por exemplo, em muitos casos, **QueryPerformanceFrequency** retorna a frequência de TSC dividida por 1024; e no Hyper-V, a frequência do contador de desempenho é sempre de 10 MHz quando a máquina virtual convidada é executada em um [hipervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) que implementa a [interface do hipervisor versão 1,0](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx). Como resultado, não presuma que **QueryPerformanceFrequency** retornará a frequência de TSC precisa.

 

O [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) lê o contador de desempenho e retorna o número total de tiques que ocorreram desde que o sistema operacional Windows foi iniciado, incluindo a hora em que o computador estava em um estado de suspensão, como em espera, hibernação ou em espera conectada.

Estes exemplos mostram como calcular o intervalo de tiques e a resolução e como converter a contagem de tiques em um valor de hora.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Exemplo 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) retorna o valor 3.125.000 em um computador específico. Qual é o intervalo de tiques e a resolução de medidas de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) neste computador? O intervalo de tiques, ou ponto, é o recíproco de 3.125.000, que é 0, 320 (320 nanossegundos). Portanto, cada tique representa a passagem de 320 nanossegundos. Intervalos de tempo menores que 320 nanossegundos não podem ser medidos neste computador.

Intervalo de escala = 1/(frequência de desempenho)

Intervalo de tiques = 1/3125000 = 320 NS

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Exemplo 2**
</dt> <dd>

No mesmo computador que o exemplo anterior, a diferença dos valores retornados de duas chamadas sucessivas para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é 5. Quanto tempo decorreu entre as duas chamadas? 5 tiques multiplicados por 320 nanossegundos geram 1,6 microssegundos.

ElapsedTime = intervalo de \* tiques de tiques

ElapsedTime = 5 \* 320 NS = 1,6 μs

</dd> </dl>

Leva tempo para acessar (ler) o contador de tique do software e esse tempo de acesso pode reduzir a precisão do tempo de medição. Isso ocorre porque o intervalo mínimo de tempo (o menor intervalo de tempo que pode ser medido) é o maior da resolução e o tempo de acesso.

Precisão = \[ resolução máxima, acessotime\]

Por exemplo, considere um temporizador de hardware hipotético com uma resolução de 100 nanossegundos e um tempo de acesso de 800 nanossegundos. Esse pode ser o caso se o temporizador de plataforma fosse usado em vez do registro TSC como a base do [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Assim, a precisão seria de 800 nanossegundos não 100 nanossegundos, conforme mostrado neste cálculo.

Precisão = máx. \[ 800 ns, 100 NS \] = 800 NS

Essas duas figuras descrevem esse efeito.

![tempo de acesso do QPC](images/qpc-access-time.png)

Se o tempo de acesso for maior do que a resolução, não tente melhorar a precisão adivinhando. Em outras palavras, é um erro supor que o carimbo de data/hora seja precisamente no meio, ou no início ou no final da chamada.

Por outro lado, considere o exemplo a seguir no qual o tempo de acesso do [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) é apenas 20 nanossegundos e a resolução do relógio do hardware é de 100 nanossegundos. Esse pode ser o caso se o registro de TSC foi usado como base para **QPC**. Aqui, a precisão é limitada pela resolução do relógio.

![precisão de QPC](images/qpc-precision.png)

Na prática, você pode encontrar fontes de tempo para as quais o tempo necessário para ler o contador é maior ou menor do que a resolução. Em ambos os casos, a precisão será a maior das duas.

Esta tabela fornece informações sobre a resolução aproximada, o tempo de acesso e a precisão de uma variedade de relógios. Observe que alguns dos valores variam com processadores diferentes, plataformas de hardware e velocidades de processador.



| Origem do relógio                                                      | Frequência nominal do relógio | Resolução do relógio    | Tempo de acesso (típico) | Precisão       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| RTC DE PC                                                            | 64 Hz                   | 15,625 milissegundos | N/D                   | N/D             |
| Contador de desempenho de consulta usando TSC com um relógio de processador de 3 GHz  | 3 MHz                   | 333 nanossegundos     | 30 nanossegundos        | 333 nanossegundos |
| Instrução de máquina **RDTSC** em um sistema com um tempo de ciclo de 3 GHz | 3 GHz                   | 333 picoseconds     | 30 nanossegundos        | 30 nanossegundos  |



 

Como o [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa um contador de hardware, ao entender algumas características básicas dos contadores de hardware, você tem noções básicas sobre os recursos e as limitações do **QPC**.

O gerador de tiques de hardware usado com mais frequência é um Oscillator do Crystal. O Crystal é uma pequena parte do Quartz ou outro material de Ceramic que exibe as características do piezoelectric que fornecem uma referência de frequência de baixo custo com excelente estabilidade e precisão. Essa frequência é usada para gerar os tiques contados pelo relógio.

A precisão de um temporizador refere-se ao grau de conformidade com um valor verdadeiro ou padrão. Isso depende principalmente da capacidade do Crystal Oscillator de fornecer tiques na frequência especificada. Se a frequência de oscilação for muito alta, o relógio será executado rapidamente, e os intervalos medidos aparecerão mais tempo do que realmente; e se a frequência for muito baixa, o relógio será executado lentamente e os intervalos medidos aparecerão mais curtos do que realmente.

Para medições de intervalo de tempo típicas por duração curta (por exemplo, medidas de tempo de resposta, medições de latência de rede e assim por diante), a precisão do Oscillator de hardware geralmente é suficiente. No entanto, para algumas medições, a precisão da frequência de Oscillator se torna importante, particularmente para intervalos de tempo longos ou quando você deseja comparar as medidas tomadas em máquinas diferentes. O restante desta seção explora os efeitos da precisão do Oscillator.

A frequência de Crystals ' oscilação é definida durante o processo de fabricação e é especificada pelo fabricante em termos de uma frequência especificada, mais ou menos uma tolerância de fabricação expressa em ' partes por milhão ' (ppm), chamada de deslocamento máximo de frequência. Um Crystal com uma frequência especificada de 1 milhão Hz e um deslocamento de frequência máximo de ± 10 ppm estaria dentro dos limites de especificação se sua frequência real estivesse entre 999.990 Hz e 1.000.010 Hz.

Ao substituir as partes de frase por milhão com microssegundos por segundo, podemos aplicar esse erro de deslocamento de frequência às medições de intervalo de tempo. Um Oscillator com um deslocamento de + 10 ppm teria um erro de 10 microssegundos por segundo. Da mesma forma, ao medir um intervalo de 1 segundo, ele seria executado rapidamente e mede um intervalo de 1 segundo como 0,999990 segundos.

Uma referência conveniente é que um erro de frequência de 100 ppm causa um erro de 8,64 segundos após 24 horas. Esta tabela apresenta a incerteza de medida devido ao erro acumulado para intervalos de tempo mais longos.



| Duração do intervalo de tempo | Incerteza de medida devido a um erro acumulado com tolerância a frequência +/-10 PPM |
|------------------------|--------------------------------------------------------------------------------------|
| 1 microssegundo          | ± 10 picoseconds (10-12)                                                             |
| 1 milissegundo          | ± 10 nanossegundos (10-9)                                                              |
| 1 segundo               | ± 10 microssegundos                                                                    |
| 1 hora                 | ± 60 microssegundos                                                                    |
| 1 dia                  | ± 0,86 segundos                                                                       |
| Uma semana                 | ± 6, 8 segundos                                                                       |



 

A tabela anterior mostra que, para intervalos de tempo pequenos, o erro de deslocamento de frequência geralmente pode ser ignorado. No entanto, para intervalos de tempo longos, mesmo um pequeno deslocamento de frequência pode resultar em uma incerteza de medida substancial.

O Crystal osciladores que são usados em computadores e servidores pessoais normalmente são fabricados com uma tolerância a frequência de ± 30 a 50 partes por milhão e raramente, Crystals pode ser desativado em até 500 ppm. Embora Crystals com tolerâncias de deslocamento de frequência muito mais rígidas estejam disponíveis, eles são mais caros e, portanto, não são usados na maioria dos computadores.

Para reduzir os efeitos adversos desse erro de deslocamento de frequência, as versões recentes do Windows, especialmente o Windows 8, usam vários temporizadores de hardware para detectar o deslocamento de frequência e compensar isso na extensão possível. Esse processo de calibragem é executado quando o Windows é iniciado.

Como mostram os exemplos a seguir, o erro de deslocamento de frequência de um relógio de hardware influencia a precisão atingível e a resolução do relógio pode ser menos importante.

![o erro de deslocamento de frequência influencia a precisão Obtida](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Exemplo 1**
</dt> <dd>

Suponha que você execute medidas de intervalo de tempo usando um Oscillator de 1 MHz, que tem uma resolução de 1 microssegundo e um erro de deslocamento de frequência máximo de ± 50 ppm. Agora, vamos supor que o deslocamento é exatamente + 50 ppm. Isso significa que a frequência real seria de 1.000.050 Hz. Se medimos um intervalo de tempo de 24 horas, nossa medição seria de 4,3 segundos muito curta (23:59:55.700000 medido versus 24:00:00.000000 real).

Segundos em um dia = 86400

Erro de deslocamento de frequência = 50 ppm = 0, 5

86.400 segundos \* 0, 5 = 4,3 segundos

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Exemplo 2**
</dt> <dd>

Suponha que o relógio de sincronismo do processador seja controlado por um Oscillator de cristal e tenha especificado a frequência de 3 GHz. Isso significa que a resolução seria 1/3000000000 ou cerca de 333 picoseconds. Suponha que o Crystal usado para controlar o relógio do processador tenha uma tolerância a frequência de ± 50 ppm e seja, na verdade, + 50 ppm. Apesar da resolução impressionante, uma medição de intervalo de tempo de 24 horas ainda será de 4,3 segundos muito curta. (23:59:55.7000000000 medido versus 24:00:00.0000000000 real).

Segundos em um dia = 86400

Erro de deslocamento de frequência = 50 ppm = 0, 5

86.400 segundos \* 0, 5 = 4,3 segundos

Isso mostra que um relógio de TSC de alta resolução não fornece necessariamente medidas mais precisas do que um clock de resolução menor.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Exemplo 3**
</dt> <dd>

Considere o uso de dois computadores diferentes para medir o mesmo intervalo de 24 horas. Ambos os computadores têm um Oscillator com um deslocamento de frequência máximo de ± 50 ppm. De que distância a medição pode ser a medida do mesmo intervalo de tempo nesses dois sistemas? Como nos exemplos anteriores, ± 50 ppm produz um erro máximo de ± 4,3 segundos após 24 horas. Se um sistema executar 4,3 segundos rapidamente e os outros 4,3 segundos mais lentos, o erro máximo após 24 horas poderá ser de 8,6 segundos.

Segundos em um dia = 86400

Erro de deslocamento de frequência = ± 50 ppm = ± 0, 5

± (86.400 segundos \* 0, 5) = ± 4,3 segundos

Deslocamento máximo entre os dois sistemas = 8,6 segundos

Em resumo, o erro de deslocamento de frequência se torna cada vez mais importante ao medir intervalos de tempo longos e ao comparar medições entre sistemas diferentes.

A estabilidade de um temporizador descreve se a frequência de tiques muda ao longo do tempo, por exemplo, como resultado de alterações de temperaturas. Os Crystals de Quartz usados como os geradores de tiques em computadores exibirão pequenas alterações na frequência como uma função de temperatura. O erro causado por descompasso térmica normalmente é pequeno em comparação com o erro de deslocamento de frequência para intervalos de temperatura comuns. No entanto, os designers de software para equipamentos portáteis ou equipamentos sujeitos a flutuações de temperatura grande podem precisar considerar esse efeito.

</dd> </dl>

## <a name="hardware-timer-info"></a>Informações do timer de hardware

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Registro de TSC**
</dt> <dd>

Alguns processadores Intel e AMD contêm um registro de TSC que é um registro de 64 bits que aumenta em uma taxa alta, normalmente igual ao relógio do processador. O valor desse contador pode ser lido pelas instruções do computador **RDTSC** ou **RDTSCP** , fornecendo tempo de acesso muito baixo e custo computacional na ordem de dezenas ou centenas de ciclos de máquina, dependendo do processador.

Embora o registro de TSC pareça um mecanismo de carimbo de data/hora ideal, aqui estão as circunstâncias em que ele não funciona de forma confiável para fins de manutenção:

-   Nem todos os processadores têm registros de TSC, portanto, usar o registro de TSC no software cria diretamente um problema de portabilidade. (O Windows selecionará uma fonte de tempo alternativa para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) nesse caso, o que evita o problema de portabilidade.)
-   Alguns processadores podem variar a frequência do relógio de TSC ou parar o avanço do registro de TSC, o que torna o TSC inadequado para fins de tempo nesses processadores. Esses processadores são considerados como registros TSC não invariáveis. (O Windows detectará isso automaticamente e selecionará uma fonte de tempo alternativa para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Em sistemas com vários processadores ou vários núcleos, alguns processadores e sistemas não podem sincronizar os relógios de cada núcleo com o mesmo valor. (O Windows detectará isso automaticamente e selecionará uma fonte de tempo alternativa para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Em alguns sistemas grandes de vários processadores, talvez você não consiga sincronizar os relógios do processador com o mesmo valor, mesmo que o processador tenha um TSC invariável. (O Windows detectará isso automaticamente e selecionará uma fonte de tempo alternativa para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Alguns processadores executarão instruções fora de ordem. Isso pode resultar em contagens de ciclo incorretas quando **RDTSC** é usado para sequências de instrução de tempo, pois a instrução **RDTSC** pode ser executada em um horário diferente do especificado em seu programa. A instrução **RDTSCP** foi introduzida em alguns processadores em resposta a esse problema.

Como outros temporizadores, o TSC é baseado em um Crystal Oscillator cuja frequência exata não é conhecida com antecedência e que tem um erro de deslocamento de frequência. Portanto, antes de poder ser usado, ele deve ser calibrado usando outra referência de tempo.

Durante a inicialização do sistema, o Windows verifica se o TSC é adequado para fins de tempo e executa a verificação de frequência e a sincronização de núcleo necessárias.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Relógio PM**
</dt> <dd>

O temporizador ACPI, também conhecido como relógio PM, foi adicionado à arquitetura do sistema para fornecer carimbos de data/hora confiáveis independentemente da velocidade dos processadores. Como esse era o único objetivo desse temporizador, ele fornece um carimbo de data/hora em um único ciclo de relógio, mas não fornece nenhuma outra funcionalidade.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**Temporizador HPET**
</dt> <dd>

O HPET (temporizador de eventos de alta precisão) foi desenvolvido em conjunto pela Intel e pela Microsoft para atender aos requisitos de tempo de multimídia e outros aplicativos sensíveis ao tempo. O suporte a HPET foi feito no Windows desde o Windows Vista, e a certificação de logotipo de hardware do Windows 7 e do Windows 8 requer suporte de HPET na plataforma de hardware.

</dd> </dl>

 

 
