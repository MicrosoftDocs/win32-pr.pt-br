---
description: Os contadores são usados para fornecer informações sobre o desempenho do sistema operacional ou de um aplicativo, serviço ou driver.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Sobre contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dec7c71e99ab614ee64e3d1e8c9620f0be78c14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828398"
---
# <a name="about-performance-counters"></a>Sobre contadores de desempenho

Os contadores de desempenho do Windows fornecem uma camada de abstração de alto nível com uma interface consistente para coletar vários tipos de dados do sistema, como estatísticas de uso de CPU, memória e disco. Os administradores de sistema usam contadores de desempenho para monitorar problemas de desempenho ou comportamento. Os desenvolvedores de software usam contadores de desempenho para inspecionar o uso de recursos de seus componentes.

> [!IMPORTANT]
> Os contadores de desempenho do Windows são otimizados para descoberta e coleta de dados administrativos/de diagnóstico. Eles não são apropriados para a coleta de dados de alta frequência ou para a criação de perfil de aplicativo, pois não foram projetados para serem coletados mais de uma vez por segundo. Para obter acesso de baixa sobrecarga às informações do sistema, você pode preferir APIs mais diretas, como [**auxiliar de status de processo**](../psapi/process-status-helper.md), [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex), [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)ou [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes). Para a criação de perfil, você pode coletar logs do ETW com dados de criação de perfil do sistema usando [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) com `-critsec` `-dpcisr` as opções,, ou `-eflag` `-ProfileSource` , ou você pode usar a [**criação de perfil de contador de hardware**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> Não confunda contadores de desempenho do Windows com a API [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) . Os contadores de desempenho do Windows fornecem uma abstração de alto nível para muitos tipos de informações do sistema. A função QueryPerformanceCounter fornece acesso otimizado a um carimbo de data/hora de alta precisão.

## <a name="getting-started"></a>Introdução

- Use as [Ferramentas do contador de desempenho](performance-counters-tools.md) quando desejar coletar ou exibir os dados de desempenho de um sistema.
- Use as [APIs de coleta do contador de desempenho](consuming-counter-data.md) quando desejar escrever um script ou um programa que coleta dados de desempenho do sistema local.
- Use as [classes do contador de desempenho do WMI](/windows/desktop/WmiSdk/monitoring-performance-data) quando desejar coletar dados de desempenho de um sistema local ou remoto usando o WMI.
- Use as [APIs do provedor de contador de desempenho](providing-counter-data.md) quando desejar publicar dados de desempenho do seu componente de software.

## <a name="concepts"></a>Conceitos

O sistema do contador de desempenho do Windows é organizado em **consumidores**, **provedores**, **conjuntos** de contracoleções, **contadores**, **instâncias** e **valores de contador**.

Um **consumidor** é um componente de software que utiliza dados de desempenho. O Windows inclui várias [ferramentas internas](performance-counters-tools.md) que fazem uso de dados de desempenho. Isso inclui o Gerenciador de tarefas, Monitor de Recursos, monitor de desempenho, typeperf.exe, logman.exe e relog.exe. Os desenvolvedores podem gravar scripts e aplicativos que acessam contadores de desempenho por meio de [APIs de contador de desempenho](consuming-counter-data.md).

Um **provedor** é um componente de software que [gera e publica dados de desempenho](providing-counter-data.md). Um provedor publicará dados para um ou mais *conjuntos* de linhas. Por exemplo, um sistema de banco de dados pode se registrar como um provedor de dado de desempenho.

- Um **provedor v1** é um componente de software que publica dados de desempenho por meio de uma [dll de desempenho](providing-counter-data-using-a-performance-dll.md) que é executada no processo do consumidor. Um provedor v1 é instalado em um sistema por meio de um `.ini` arquivo. A arquitetura do provedor v1 foi preterida. Novos provedores devem usar a arquitetura do provedor v2.
- Um **provedor v2** é um componente de software que publica dados de desempenho por meio das [APIs do provedor de contador de desempenho](providing-counter-data-using-version-2-0.md). Um provedor V2 é instalado em um sistema por meio de um `.man` arquivo (manifesto XML).

Um **CounterSet** é um agrupamento de dados de desempenho dentro de um provedor. Um CounterSet tem um nome e um ou mais *contadores*. A coleta de dados de um CounterSet retorna um número de *instâncias*. Em algumas APIs do Windows, os conjuntos de contraissores são chamados de **objetos de desempenho**. Por exemplo, um provedor de dados de desempenho para um sistema de banco de dado pode fornecer um CounterSet para estatísticas por banco de dados.

Um **contador** é a definição de um único dado de desempenho. Um contador tem um nome e um tipo. Por exemplo, um CounterSet "estatísticas por banco de dados" pode conter um contador chamado "transações por segundo" com o tipo `PERF_COUNTER_COUNTER` .

Uma **instância** é uma entidade sobre a qual os dados de desempenho são relatados. Uma instância tem um nome (cadeia de caracteres) e um ou mais *valores de contador*. Por exemplo, um CounterSet "estatísticas por banco de dados" pode conter uma instância por banco de dados. O nome da instância seria o nome do banco de dados, e cada instância conteria valores de contador para os contadores "transações por segundo", "uso de memória" e "uso do disco".

Um **valor de contador** é o valor de uma única parte dos dados do contador de desempenho. Um valor de contador é um inteiro não assinado, de 32 bits ou de 64 bits, dependendo do tipo do contador correspondente. Ao falar sobre uma *instância*, um *valor de contador* pode, às vezes, ser chamado de *contador* ou *valor*.

> [!TIP]
> Pode ser útil relacionar os termos do contador de desempenho a termos de planilha mais familiares. Um **CounterSet** é como uma tabela. Um **contador** é como uma coluna. Uma **instância** é como uma linha. Um **valor de contador** é como uma célula na tabela.

Os **conjuntos de itens de instância única** sempre contêm dados para exatamente uma instância. Isso é comum para conjuntos de linhas que relatam estatísticas globais do sistema. Por exemplo, o Windows tem um contador de instância única interno chamado "memória" que relata o uso de memória global.

Os **conjuntos de contrainstâncias de várias** instâncias contêm dados para um número variável de instâncias. Isso é comum para conjuntos de linhas que relatam sobre entidades no sistema. Por exemplo, o Windows tem um contador de várias instâncias interno chamado "informações do processador" que relata uma instância para cada CPU instalada.

Os consumidores coletarão e registrarão periodicamente os dados do contador de contadores de um provedor. Por exemplo, o consumidor pode coletar dados uma vez por segundo ou uma vez por minuto. Os dados coletados são chamados de **exemplo**. Um exemplo consiste em carimbos de data/hora junto com os dados para instâncias do CounterSet. Os dados de cada instância incluem o nome da instância (cadeia de caracteres) e um conjunto de valores de contadores (inteiros, um valor para cada contador no CounterSet).

Nomes de instância normalmente devem ser exclusivos em um exemplo, ou seja, um provedor não deve retornar duas instâncias com o mesmo nome que parte de um único exemplo. Alguns provedores mais antigos não seguem essa regra, portanto, os [consumidores devem ser capazes de tolerar nomes de instância não exclusivos](handling-duplicate-instance-names.md). Os nomes de instância não diferenciam maiúsculas de minúsculas, portanto, as instâncias não devem ter nomes que diferem apenas no caso.

> [!NOTE]
> Para fins de compatibilidade com versões anteriores, o CounterSet "processo" retorna nomes de instância não exclusivos com base no nome de arquivo EXE. Isso pode causar resultados confusos, especialmente quando um processo com um nome não exclusivo é iniciado ou desligado, pois isso normalmente resultará em problemas de dados devido à correspondência incorreta de nomes de instância entre exemplos. Os consumidores do CounterSet "processo" devem ser capazes de tolerar esses nomes de instância não exclusiva e os problemas de dados resultantes.

Os nomes de instância devem ser estáveis entre amostras, ou seja, um provedor deve usar o mesmo nome de instância para a mesma entidade sempre que o CounterSet for coletado.

Cada contador tem um tipo. O tipo de contador indica o tipo de **valor bruto** do contador (inteiro de 32 bits sem sinal ou um inteiro de 64 bits não assinado). O tipo de contador também indica o que o valor bruto do contador representa, que determina como o valor bruto deve ser processado para gerar estatísticas úteis.

Embora alguns tipos de contadores sejam simples e tenham um valor bruto que seja diretamente útil, muitos tipos de contadores exigem [processamento adicional](calculating-counter-values.md) para criar um **valor formatado** útil. Para produzir o valor formatado, alguns tipos de contadores exigem valores brutos de dois exemplos, alguns tipos de contadores exigem carimbos de data/hora e alguns tipos de contadores exigem valores brutos de vários contadores. Por exemplo:

- `PERF_COUNTER_LARGE_RAWCOUNT` é um valor bruto de 64 bits que não requer nenhum processamento para ser útil. É apropriado para valores de ponto no tempo, como "bytes de memória em uso".
- `PERF_COUNTER_RAWCOUNT_HEX` é um valor bruto de 32 bits que requer que apenas formatação hexadecimal simples seja útil. Ele é apropriado para o ponto no tempo ou para identificar informações como "Flags" ou "endereço base".
- `PERF_COUNTER_BULK_COUNT` é um valor bruto de 64 bits que indica uma contagem de eventos e é usado para calcular a taxa na qual os eventos ocorrem. Para ser útil, esse tipo de contador requer dois exemplos separados no tempo. O valor formatado é a taxa de evento, ou seja, o número de vezes que o evento ocorreu por segundo no intervalo entre os dois exemplos. Considerando dois exemplos `s0` e `s1` , o valor formatado (taxa de evento) seria calculado como `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Os provedores devem se comportar como se fossem sem estado, ou seja, coletar dados de um CounterSet não deve afetar visivelmente o estado do provedor. Por exemplo, um provedor não deve redefinir valores de contador como 0 quando um CounterSet é coletado e não deve usar o carimbo de data/hora de uma coleção anterior para ajustar os valores na coleção atual. Em vez disso, ele deve fornecer valores de contador brutos simples com tipos precisos para que o consumidor possa calcular estatísticas úteis com base nos valores brutos e seus carimbos de data/hora.

## <a name="performance-api-architecture"></a>Arquitetura da API de desempenho

![Os aplicativos do contador de desempenho chamam APIs do Windows que chamam provedores para obter dados de desempenho.](images/architecture.png)

Os consumidores do contador de desempenho incluem:

- [Aplicativos fornecidos pela Microsoft](performance-counters-tools.md) , como o Gerenciador de tarefas, monitor de recursos, monitor de desempenho e typeperf.exe.
- As superfícies de API de alto nível fornecidas pela Microsoft que expõem dados do contador de desempenho, como [classes de desempenho WMI](/windows/desktop/WmiSdk/monitoring-performance-data).
- Seus próprios aplicativos ou scripts que usam as [APIs de consumidor do contador de desempenho](consuming-counter-data.md).

A maioria dos consumidores do contador de desempenho usa APIs de [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) para coletar dados de desempenho. A PDH gerencia muitos aspectos complexos da coleta de contadores de desempenho, como a análise de consultas, a correspondência de instâncias em vários exemplos e a computação de valores formatados dos dados brutos do contador. A implementação da PDH usa as APIs do registro ao consumir dados de um provedor v1 e usa as APIs de consumidor v2 ao consumir dados de um provedor v2.

Alguns consumidores mais antigos do contador de desempenho usam as [APIs do registro](using-the-registry-functions-to-consume-counter-data.md) para coletar dados de desempenho da `HKEY_PERFORMANCE_DATA` chave do registro especial. Isso não é recomendado para o novo código porque o processamento dos dados do registro é complexo e propenso a erros. A implementação da API do registro diretamente dá suporte à coleta de dados de provedores v1. Ele é compatível indiretamente com a coleta de dados de provedores v2 por meio de uma camada de conversão que usa as APIs de consumidor v2.

Alguns consumidores do contador de desempenho usam as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) para acessar diretamente os dados de provedores v2. Isso é mais complexo do que consumir dados usando as APIs de PDH, mas essa abordagem pode ser útil se as APIs de PDH não puderem ser usadas devido a questões de desempenho ou dependência. A implementação de PerfLib v2 dá suporte diretamente à coleta de dados de provedores v2. Ele não dá suporte à coleta de dados de provedores v1.

> [!NOTE]
> O Windows OneCore não inclui PDH.dll e não inclui suporte para o consumo de dados do contador de desempenho por meio das APIs do registro. Os consumidores em execução no OneCore devem usar as funções de consumidor do PerfLib v2.

Os provedores v1 são implementados como uma DLL de provedor que é carregada no processo do consumidor. A implementação da API do registro gerencia o carregamento da DLL do provedor, chamando a DLL para coletar dados de desempenho e descarregar a DLL conforme apropriado. A DLL do provedor é responsável por [coletar dados de desempenho conforme apropriado](communicating-with-your-application.md), por exemplo, usando APIs normais do Windows, RPC, pipes nomeados, memória compartilhada ou outros mecanismos de comunicação entre processos.

Os provedores v2 são implementados como um programa de modo de usuário (geralmente um serviço do Windows) ou um driver de modo kernel. Normalmente, o código do provedor de dados de desempenho é integrado diretamente a um componente existente (ou seja, o driver ou o serviço está relatando estatísticas sobre si mesmo). A implementação da PerfLib v2 gerencia solicitações e respostas por meio da extensão do kernel PCW.sys, de modo que o provedor geralmente não precisa implementar nenhuma comunicação entre processos para fornecer os dados de desempenho.

> [!NOTE]
> Ferramentas e APIs do contador de desempenho do Windows incluem suporte limitado para acessar contadores de desempenho de outros computadores por meio do registro remoto (para provedores v1) e RPC (para provedores v2). Esse suporte é muitas vezes difícil de usar em termos de controles de autenticação (as ferramentas e as APIs só podem ser autenticadas como o usuário atual), bem como em termos de [configuração do sistema](accessing-remote-counter-data.md) (os pontos de extremidade e serviços necessários são desabilitados por padrão). Em muitos casos, é melhor acessar os contadores de desempenho de sistemas remotos via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) em vez de por meio do suporte interno a acesso remoto.

## <a name="developer-audience"></a>Público de desenvolvedores

Os contadores de desempenho são frequentemente consumidos por administradores para identificar problemas de desempenho ou comportamento anormal dos sistemas, por desenvolvedores para estudar o uso de recursos de componentes de software e por usuários individuais para entender como os programas estão se comportando em seu sistema. O uso pode ocorrer por meio de ferramentas de GUI, como o Gerenciador de tarefas ou o monitor de desempenho, ferramentas de linha de comando como typeperf.exe ou logman.exe, por meio de scripts via WMI e PowerShell, ou por meio de APIs C/C++ e .NET.

Os provedores de contador de desempenho geralmente são implementados como drivers de modo kernel ou serviços de modo de usuário. Os provedores de contador de desempenho são geralmente escritos em C ou C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

Para obter o histórico de versão, consulte [novidades](performance-counters-what-s-new.md).

## <a name="see-also"></a>Confira também

[Utilizando contadores de desempenho](using-performance-counters.md)

[Referência de contadores de desempenho](performance-counters-reference.md)
