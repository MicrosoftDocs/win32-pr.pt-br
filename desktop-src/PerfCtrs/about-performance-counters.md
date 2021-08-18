---
description: Os contadores são usados para fornecer informações sobre o desempenho do sistema operacional ou de um aplicativo, serviço ou driver.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Sobre contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8a80ac907ef842e4564f0e67daa173fee165bc93d8fa568920df8ffc24b8c9a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978906"
---
# <a name="about-performance-counters"></a>Sobre contadores de desempenho

Windows Os Contadores de Desempenho fornecem uma camada de abstração de alto nível com uma interface consistente para coletar vários tipos de dados do sistema, como CPU, memória e estatísticas de uso de disco. Os administradores do sistema usam contadores de desempenho para monitorar problemas de desempenho ou comportamento. Os desenvolvedores de software usam contadores de desempenho para inspecionar o uso de recursos de seus componentes.

> [!IMPORTANT]
> Windows Os Contadores de Desempenho são otimizados para coleta e descoberta de dados administrativos/de diagnóstico. Eles não são apropriados para coleta de dados de alta frequência ou para criação de perfil de aplicativo, pois não são projetados para serem coletados mais de uma vez por segundo. Para acesso de menor sobrecarga às informações do sistema, você pode preferir APIs mais diretas, como Auxiliar de [**Status**](../psapi/process-status-helper.md)do Processo, [**GlobalMemoryStatusEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)ou [**GetProcessTimes.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes) Para criação de perfil, você pode coletar logs ETW com dados de criação de perfil do sistema [**usando**](/windows-hardware/drivers/devtest/tracelog)tracelog.execom as opções , , ou ou pode usar a Criação de Perfil `-critsec` do Contador de `-dpcisr` `-eflag` `-ProfileSource` [**Hardware**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> Não confunda Windows contadores de desempenho com a API [**QueryPerformanceCounter.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Windows Os Contadores de Desempenho fornecem uma abstração de alto nível para muitos tipos de informações do sistema. A função QueryPerformanceCounter fornece acesso otimizado a um timestamp de alta precisão.

## <a name="getting-started"></a>Introdução

- Use [as Ferramentas de Contador de](performance-counters-tools.md) Desempenho quando quiser coletar ou exibir os dados de desempenho de um sistema.
- Use [APIs de Coleta](consuming-counter-data.md) do Contador de Desempenho quando quiser escrever um script ou um programa que coleta dados de desempenho do sistema local.
- Use classes de contador de desempenho [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) quando quiser coletar dados de desempenho de um sistema local ou remoto usando o WMI.
- Use [AS APIs do Provedor](providing-counter-data.md) do Contador de Desempenho quando quiser publicar dados de desempenho do componente de software.

## <a name="concepts"></a>Conceitos

O Windows do Contador de Desempenho é organizado em **consumidores,** **provedores,** contadores, contadores,  **instâncias** e valores de **contador**.

Um **consumidor** é um componente de software que usa dados de desempenho. Windows inclui várias [ferramentas integrados](performance-counters-tools.md) que usam dados de desempenho. Isso inclui Gerenciador de Tarefas, Monitor de Recursos, Monitor de Desempenho, typeperf.exe, logman.exe e relog.exe. Os desenvolvedores podem escrever scripts e aplicativos que acessam contadores de desempenho por meio de [APIs do contador de desempenho](consuming-counter-data.md).

Um **provedor** é um componente de software [que gera e publica dados de desempenho](providing-counter-data.md). Um provedor publicará dados para um ou mais *conjuntos de contadores*. Por exemplo, um sistema de banco de dados pode se registrar como um provedor de dados de desempenho.

- Um **provedor V1 é** um componente de software que publica dados de desempenho por meio de uma [DLL](providing-counter-data-using-a-performance-dll.md) de desempenho que é executado no processo do consumidor. Um provedor V1 é instalado em um sistema por meio de um `.ini` arquivo. A arquitetura do provedor V1 foi preterida. Novos provedores devem usar a arquitetura do provedor V2.
- Um **provedor V2 é** um componente de software que publica dados de desempenho por meio das APIs do provedor do contador de [desempenho](providing-counter-data-using-version-2-0.md). Um provedor V2 é instalado em um sistema por meio de um `.man` arquivo (manifesto XML).

Um **conjunto de contadores** é um grupo de dados de desempenho dentro de um provedor. Um counterset tem um nome e um ou mais *contadores*. Coletar os dados de um counterset retorna várias *instâncias*. Em alguns Windows APIs, os conjuntos de contadores são chamados de **objetos de desempenho**. Por exemplo, um provedor de dados de desempenho para um sistema de banco de dados pode fornecer um contador para estatísticas por banco de dados.

Um **contador** é a definição de dados de desempenho único. Um contador tem um nome e um tipo. Por exemplo, um contador "estatísticas por banco de dados" pode conter um contador chamado "transações por segundo" com o tipo `PERF_COUNTER_COUNTER` .

Uma **instância** é uma entidade sobre a qual os dados de desempenho são relatados. Uma instância tem um nome (cadeia de caracteres) e um ou mais *valores de contador*. Por exemplo, um contador "estatísticas por banco de dados" pode conter uma instância por banco de dados. O nome da instância seria o nome do banco de dados e cada instância conteria valores de contador para contadores "transações por segundo", "uso de memória" e "uso de disco".

Um **valor de contador** é o valor de uma única parte dos dados do contador de desempenho. Um valor de contador é um inteiro sem sinal, de 32 bits ou de 64 bits, dependendo do tipo do contador correspondente. Ao falar sobre uma *instância*, um *valor de contador* às vezes pode ser chamado de *contador* ou *um valor*.

> [!TIP]
> Pode ser útil relacionar os termos do contador de desempenho a termos de planilha mais conhecidos. Um **counterset** é como uma tabela. Um **contador** é como uma coluna. Uma **instância** é como uma linha. Um **valor de contador** é como uma célula na tabela.

**Os contadores de instância única** sempre contêm dados para exatamente uma instância. Isso é comum para countersets que relatam estatísticas globais do sistema. Por exemplo, Windows tem um contador de instância única interna chamado "Memória" que relata o uso de memória global.

**Os conjuntos de contadores de várias instâncias** contêm dados para um número variável de instâncias. Isso é comum para countersets que relatam sobre entidades dentro do sistema. Por exemplo, Windows tem um contador de várias instâncias integrado chamado "Informações do Processador" que relata uma instância para cada CPU instalada.

Os consumidores coletarão e registrarão periodicamente os dados do contador de um provedor. Por exemplo, o consumidor pode coletar dados uma vez por segundo ou uma vez por minuto. Os dados coletados são chamados de **um exemplo**. Um exemplo consiste em timestamps juntamente com os dados para instâncias do counterset. Os dados de cada instância incluem o nome da instância (cadeia de caracteres) e um conjunto de valores de contador (inteiros, um valor para cada contador no conjunto de contadores).

Os nomes de instância normalmente devem ser exclusivos em um exemplo, ou seja, um provedor não deve retornar duas instâncias com o mesmo nome que parte de um único exemplo. Alguns provedores mais antigos não seguem essa regra, portanto, os consumidores devem ser capazes de [tolerar nomes de instância não exclusivos](handling-duplicate-instance-names.md). Nomes de instância não diferenciam minúsculas, portanto, as instâncias não devem ter nomes que diferem apenas no caso.

> [!NOTE]
> Por motivos de compatibilidade com compatibilidade regressiva, o contador "Processo" retorna nomes de instância não exclusivos com base no nome do arquivo EXE. Isso pode causar resultados confusos, especialmente quando um processo com um nome não exclusivo é iniciado ou desligado, pois isso normalmente resultará em falhas de dados devido à correspondência incorreta de nomes de instância entre amostras. Os consumidores do contador "Processo" devem ser capazes de tolerar esses nomes de instância não exclusivos e as falhas de dados resultantes.

Os nomes de instância devem ser estáveis entre amostras, ou seja, um provedor deve usar o mesmo nome de instância para a mesma entidade sempre que o contador for coletado.

Cada contador tem um tipo . O tipo de contador indica o tipo do valor bruto do contador **(inteiro** sem sinal de 32 bits ou inteiro de 64 bits sem sinal). O tipo de contador também indica qual valor bruto do contador representa, que determina como o valor bruto deve ser processado para gerar estatísticas úteis.

Embora alguns tipos de contador sejam simples e tenham um [](calculating-counter-values.md) valor bruto que seja diretamente útil, muitos tipos de contador exigem processamento adicional para criar um valor **formatado útil.** Para produzir o valor formatado, alguns tipos de contador exigem valores brutos de dois exemplos, alguns tipos de contador exigem os timestamps e alguns tipos de contador exigem valores brutos de vários contadores. Por exemplo:

- `PERF_COUNTER_LARGE_RAWCOUNT` é um valor bruto de 64 bits que não requer que nenhum processamento seja útil. É apropriado para valores de ponto no tempo, como "Bytes de memória em uso".
- `PERF_COUNTER_RAWCOUNT_HEX` é um valor bruto de 32 bits que requer que apenas a formatação hexadecimal simples seja útil. É apropriado para informações de ponto no tempo ou identificação, como "Sinalizadores" ou "Endereço Base".
- `PERF_COUNTER_BULK_COUNT` é um valor bruto de 64 bits que indica uma contagem de eventos e é usado para calcular a taxa na qual os eventos ocorrem. Para ser útil, esse tipo de contador requer dois exemplos separados no tempo. O valor formatado é a taxa de eventos, ou seja, o número de vezes que o evento ocorreu por segundo durante o intervalo entre as duas amostras. Dado dois exemplos `s0` e , o valor `s1` formatado (taxa de eventos) seria calculado como `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Os provedores devem se comportar como se eles não têm estado, ou seja, a coleta de dados de um counterset não deve afetar visivelmente o estado do provedor. Por exemplo, um provedor não deve redefinir valores de contador para 0 quando um conjunto de contadores é coletado e não deve usar o timestamp de uma coleção anterior para ajustar os valores na coleção atual. Em vez disso, ele deve fornecer valores de contador brutos simples com tipos precisos para que o consumidor possa calcular estatísticas úteis com base nos valores brutos e seus timestamps.

## <a name="performance-api-architecture"></a>Arquitetura da API de Desempenho

![Os aplicativos de contador de desempenho Windows APIs que chamam os provedores para obter dados de desempenho.](images/architecture.png)

Os consumidores do contador de desempenho incluem:

- [Aplicativos fornecidos pela Microsoft,](performance-counters-tools.md) como Gerenciador de Tarefas, Monitor de Recursos, Monitor de Desempenho e typeperf.exe.
- Superfícies de API de alto nível fornecidas pela Microsoft que expõem dados do contador de desempenho, como classes [de desempenho WMI.](/windows/desktop/WmiSdk/monitoring-performance-data)
- Seus próprios aplicativos ou scripts que usam [APIs de consumidor do contador de desempenho](consuming-counter-data.md).

A maioria dos consumidores do contador de desempenho usa APIs [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) coletar dados de desempenho. O PDH gerencia muitos aspectos complexos da coleta de contadores de desempenho, como a análise de consultas, a correspondência de instâncias em vários exemplos e a computação de valores formatados dos dados brutos do contador. A implementação de PDH usa as APIs do Registro ao consumir dados de um provedor V1 e usa as APIs de consumidor V2 ao consumir dados de um provedor V2.

Alguns consumidores mais antigos do contador de desempenho usam [as APIs](using-the-registry-functions-to-consume-counter-data.md) do Registro para coletar dados de desempenho da chave especial `HKEY_PERFORMANCE_DATA` do Registro. Isso não é recomendado para o novo código porque o processamento dos dados do Registro é complexo e propenso a erros. A implementação da API do Registro dá suporte diretamente à coleta de dados de provedores V1. Ele é compatível indiretamente com a coleta de dados de provedores v2 por meio de uma camada de conversão que usa as APIs de consumidor v2.

Alguns consumidores do contador de desempenho usam as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) para acessar diretamente os dados de provedores v2. Isso é mais complexo do que consumir dados usando as APIs de PDH, mas essa abordagem pode ser útil se as APIs de PDH não puderem ser usadas devido a questões de desempenho ou dependência. A implementação de PerfLib v2 dá suporte diretamente à coleta de dados de provedores v2. Ele não dá suporte à coleta de dados de provedores v1.

> [!NOTE]
> Windows OneCore não inclui PDH.dll e não inclui suporte para o consumo de dados do contador de desempenho por meio das APIs do registro. os consumidores em execução no OneCore devem usar as funções de consumidor do PerfLib V2.

Os provedores v1 são implementados como uma DLL de provedor que é carregada no processo do consumidor. A implementação da API do registro gerencia o carregamento da DLL do provedor, chamando a DLL para coletar dados de desempenho e descarregar a DLL conforme apropriado. a DLL do provedor é responsável por [coletar dados de desempenho conforme apropriado](communicating-with-your-application.md), por exemplo, usando APIs de Windows normais, RPC, pipes nomeados, memória compartilhada ou outros mecanismos de comunicação entre processos.

os provedores V2 são implementados como um programa de modo de usuário (geralmente um serviço Windows) ou um driver de modo kernel. Normalmente, o código do provedor de dados de desempenho é integrado diretamente a um componente existente (ou seja, o driver ou o serviço está relatando estatísticas sobre si mesmo). A implementação da PerfLib v2 gerencia solicitações e respostas por meio da extensão do kernel PCW.sys, de modo que o provedor geralmente não precisa implementar nenhuma comunicação entre processos para fornecer os dados de desempenho.

> [!NOTE]
> Windows APIs e ferramentas do contador de desempenho incluem suporte limitado para acessar contadores de desempenho de outros computadores por meio do registro remoto (para provedores v1) e RPC (para provedores v2). Esse suporte é muitas vezes difícil de usar em termos de controles de autenticação (as ferramentas e as APIs só podem ser autenticadas como o usuário atual), bem como em termos de [configuração do sistema](accessing-remote-counter-data.md) (os pontos de extremidade e serviços necessários são desabilitados por padrão). Em muitos casos, é melhor acessar os contadores de desempenho de sistemas remotos via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) em vez de por meio do suporte interno a acesso remoto.

## <a name="developer-audience"></a>Público de desenvolvedores

Os contadores de desempenho são frequentemente consumidos por administradores para identificar problemas de desempenho ou comportamento anormal dos sistemas, por desenvolvedores para estudar o uso de recursos de componentes de software e por usuários individuais para entender como os programas estão se comportando em seu sistema. O uso pode ocorrer por meio de ferramentas de GUI, como o Gerenciador de tarefas ou o monitor de desempenho, ferramentas de linha de comando como typeperf.exe ou logman.exe, por meio de scripts via WMI e PowerShell, ou por meio de APIs C/C++ e .NET.

Os provedores de contador de desempenho geralmente são implementados como drivers de modo kernel ou serviços de modo de usuário. Os provedores de contador de desempenho são geralmente escritos em C ou C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

Para obter o histórico de versão, consulte [novidades](performance-counters-what-s-new.md).

## <a name="see-also"></a>Confira também

[Utilizando contadores de desempenho](using-performance-counters.md)

[Referência de contadores de desempenho](performance-counters-reference.md)
