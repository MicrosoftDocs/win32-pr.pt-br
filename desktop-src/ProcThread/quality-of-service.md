---
description: A qualidade do serviço indica o desempenho e a eficiência de energia de um thread, o que pode influenciar o agendamento de threads e o gerenciamento de energia do processador.
title: Qualidade de Serviço
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: ec4e92360d23a427d526a36a81bfdb0667c1cb6fb5f60ddcefd578c4918ba5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793460"
---
# <a name="quality-of-service"></a>Qualidade de Serviço

A QoS (qualidade de serviço) associada a um thread é usada para indicar o desempenho desejado e a eficiência de energia. Cada thread é atribuído a um nível de QoS. Embora a prioridade de agendamento permaneça a principal métrica pela qual o sistema determina qual thread deve ser agendado em seguida, a QoS pode influenciar a seleção de núcleos e o gerenciamento de energia do processador. Em plataformas com processadores heterogêneos, a QoS de um thread pode restringir o agendamento a um subconjunto de processadores ou indicar uma preferência para uma classe específica de processador.

Os desenvolvedores podem já estar empregando outros recursos para controlar quando executar o, por exemplo, quando o usuário não está presente, somente em AC/cobrança ou dependendo do nível da bateria. A QoS fornece uma instalação para influenciar a execução. Esse recurso pode ajudar a melhorar a eficiência da CPU e, portanto, estender a vida útil da bateria. Além disso, esse processo pode ajudar a reduzir o consumo de energia da CPU enquanto opera em energia CA para reduzir a saída térmica, o que pode levar a um ruído de ventilador alto ou até mesmo limitação térmica.

## <a name="quality-of-service-levels"></a>Qualidade dos níveis de serviço

O sistema mantém vários níveis de QoS, cada um com desempenho diferenciado e eficiência de energia. Windows fornece configurações padrão para agendamento e gerenciamento de energia de processador para cada nível de QoS. o ajuste preciso de cada nível de QoS para o gerenciamento de energia do processador e o agendamento heterogêneo pode ser modificado por meio do provisionamento de Windows. Para obter mais informações sobre o ajuste de desempenho e o provisionamento, consulte [Opções de gerenciamento de energia do processador](/windows-hardware/customize/power-settings/configure-processor-power-management-options).

| Nível de QoS | Descrição|Desempenho e energia | Versão |
| --- | --- | --- | --- |
| Alto | Aplicativos em janelas que estão nos processos de primeiro plano e em foco, ou audível e explicitamente marcam com [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) ou threads com [SetThreadInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation) | Alto desempenho padrão. |1.709 |
| Médio | Aplicativos em janelas que podem estar visíveis para o usuário final, mas que não estão em foco. | Varia de acordo com a plataforma, entre alta e baixa. | 1.709 |
| Baixo | Aplicativos em janelas que não são visíveis ou audíveis para o usuário final. | Na bateria, seleciona a frequência de CPU e agendas mais eficientes para núcleo eficiente. | 1.709 |
| Meio ambiente | Aplicativos que marcam explicitamente os processos com [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) ou threads com [SetThreadInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation). | Sempre seleciona a frequência de CPU e agendas mais eficientes para núcleos eficientes. | Windows 11 |
| Mídia | Threads explicitamente marcados pelo [serviço de Agendador de classes de multimídia](/windows/desktop/procthread/multimedia-class-scheduler-service) para indicar buffer de lote de multimídia. | Frequência de CPU reduzida para processamento em lote eficiente. | 2004 |
| Prazo | Threads explicitamente marcados pelo [serviço de Agendador de classes de multimídia](/windows/desktop/procthread/multimedia-class-scheduler-service) para indicar que os threads de áudio exigem desempenho para atender aos prazos. | Alto desempenho para atender aos prazos de mídia. | 2004 |

## <a name="quality-of-service-classification"></a>Qualidade de classificação de serviço

A tabela a seguir mostra as classificações de QoS com suporte.

| Fonte | Descrição |
| --- | --- |
| Base de multimídia | O [serviço do Agendador de classes de multimídia](/windows/desktop/procthread/multimedia-class-scheduler-service) prioriza os recursos de CPU para cenários de multimídia. O serviço marca os threads específicos responsáveis pelo processamento de multimídia usando os níveis de QoS de mídia e prazo para fornecer eficiência de energia enquanto atende aos prazos de desempenho.  |
| API | O [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) permite que os desenvolvedores marquem explicitamente um processo como HighQoS ou EcoQoS alternando o `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` recurso no **ProcessPowerThrottling**.</br>O [SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) permite que os desenvolvedores marquem explicitamente um thread como HighQoS ou EcoQoS alternando o `THREAD_POWER_THROTTLING_EXECUTION_SPEED` recurso no **ThreadPowerThrottling** .  |
| Sonoro | Os processos que são determinados para a reprodução de áudio são HighQoS. |
| Visible | Os processos que possuem diretamente uma janela (ou são descendentes de processos de propriedade da janela) recebem um nível de QoS de acordo com seu estado de visibilidade e foco:</br></br><table><tr><th>Estado da janela</th><th>Qualidade de Serviço</th></tr><tr><td>Em foco</td><td>Alto</td></tr><tr><td>Visible</td><td>Médio</td></tr><tr><td>Minimizado, ou totalmente obstruído</td><td>Baixo</td></tr></table> |
| Heurística | Os threads que não são classificados pelas fontes acima recebem automaticamente um nível de QoS pelo sistema. Essas heurísticas incluem (mas não se limitam a) a prioridade de thread, em que os threads em execução com prioridade de thread reduzida podem implicar em um nível inferior de QoS. |
