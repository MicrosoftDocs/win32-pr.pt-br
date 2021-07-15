---
description: Qualidade de Serviço indica o desempenho e a eficiência de energia de um thread, o que pode influenciar o agendamento de threads e o gerenciamento de energia do processador.
title: Qualidade de Serviço
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: c506e810bafad41e9a5f14112c1398b0d6fb3ffc
ms.sourcegitcommit: 2805e19a2738a408d3c5ab69a8d84ec92ca25e36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/14/2021
ms.locfileid: "113989784"
---
# <a name="quality-of-service"></a>Qualidade de Serviço

A QoS (Qualidade de Serviço) associada a um thread é usada para indicar o desempenho desejado e a eficiência de energia. Cada thread é atribuído a um nível de QoS. Embora a prioridade de agendamento permaneça a principal métrica pela qual o sistema determina qual thread agendar em seguida, a QoS pode influenciar a seleção principal e o gerenciamento de energia do processador. Em plataformas com processadores heterogêneos, a QoS de um thread pode restringir o agendamento a um subconjunto de processadores ou indicar uma preferência para uma classe específica de processador.

Os desenvolvedores já podem estar empregando outros recursos para controlar quando executar, como quando o usuário não está presente, somente na AC/carregamento ou dependendo do nível da bateria. A QoS fornece uma instalação para influenciar a execução. Esse recurso pode ajudar a melhorar a eficiência da CPU e, portanto, estender a vida útil da bateria. Além disso, esse processo pode ajudar a reduzir o consumo de energia da CPU enquanto opera na energia de AC para reduzir a saída térmica, o que pode levar a um alto ruído de ventilador ou até mesmo à sobrecarga térmica.

## <a name="quality-of-service-levels"></a>Níveis de qualidade de serviço

O sistema mantém vários níveis de QoS, cada um com desempenho diferenciado e eficiência de energia. Windows fornece configurações padrão para agendamento e gerenciamento de energia do processador para cada nível de QoS. O ajuste preciso de cada nível de QoS para gerenciamento de energia do processador e agendamento heterogêneo pode ser modificado por meio Windows Provisionamento. Para obter mais informações sobre o provisionamento e ajuste de desempenho, consulte [Opções de gerenciamento de energia do processador](/windows-hardware/customize/power-settings/configure-processor-power-management-options).

| Nível de QoS | Descrição|Desempenho e potência | Versão |
| --- | --- | --- | --- |
| Alto | Aplicativos em janelas que estão em primeiro plano e em foco ou audíveis | Alto desempenho padrão |1.709 |
| Médio | Aplicativos em janelas que podem estar visíveis para o usuário final, mas não estão em foco | Varia de acordo com a plataforma, entre Alta e Baixa | 1.709 |
| Baixo | Aplicativos em janelas que não são visíveis ou audíveis para o usuário final | Na bateria, seleciona a frequência de CPU e agendamentos mais eficientes para núcleos eficientes | 1.709 |
| Eco | Aplicativos que marcam explicitamente processos [com SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) ou threads com [SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) | Sempre seleciona a frequência de CPU e agendamentos mais eficientes para núcleos eficientes | Windows 11 |
| Mídia | Threads explicitamente marcados pelo Serviço de [Agendador](/windows/desktop/procthread/multimedia-class-scheduler-service) de Classe Multimídia para denotar o buffer em lote multimídia | Frequência de CPU reduzida para processamento em lote eficiente | 2004 |
| Prazo | Threads explicitamente marcados pelo Serviço de [Agendador](/windows/desktop/procthread/multimedia-class-scheduler-service) de Classe Multimídia para indicar que os threads de áudio exigem desempenho para atender aos prazos | Alto desempenho para atender aos prazos de mídia | 2004 |

## <a name="quality-of-service-classification"></a>Classificação de qualidade de serviço

A tabela a seguir mostra as classificações de QoS com suporte.

| Fonte | Descrição |
| --- | --- |
| Multimídia Foundation | O [Serviço de Agendador de Classes Multimídia](/windows/desktop/procthread/multimedia-class-scheduler-service) prioriza recursos de CPU para cenários multimídia. O serviço marca threads específicos responsáveis pelo processamento multimídia usando os níveis de QoS de Mídia e Prazo para fornecer eficiência de energia ao atender aos prazos de desempenho.  |
| API | [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) permite que os desenvolvedores marquem explicitamente um processo como HighQoS ou EcoQoS, agregação do recurso `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` **em ProcessPowerThrottling.**</br>[SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) permite que os desenvolvedores marquem explicitamente um thread como HighQoS ou EcoQoS ao efetuar a agregação do recurso `THREAD_POWER_THROTTLING_EXECUTION_SPEED` **em ThreadPowerThrottling.**  |
| Audível | Os processos que são determinados para reprodução de áudio são HighQoS. |
| Visible | Processos que têm diretamente uma janela (ou são descendentes de processos de propriedade de janela) são atribuídos a um nível de QoS de acordo com sua visibilidade e estado de foco:</br></br><table><tr><th>Estado da janela</th><th>Qualidade de Serviço</th></tr><tr><td>Em foco</td><td>Alto</td></tr><tr><td>Visible</td><td>Médio</td></tr><tr><td>Minimizado ou Totalmente Ocluso</td><td>Baixo</td></tr></table> |
| Heurística | Threads que não são classificados pelas fontes acima são atribuídos automaticamente a um nível de QoS pelo sistema. Essas heurísticas incluem (mas não estão limitadas a) prioridade de thread, em que threads em execução com prioridade de thread reduzido podem implicar um nível de QoS inferior. |
