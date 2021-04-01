---
description: O serviço do Agendador de classes de multimídia (MMCSS) permite que os aplicativos multimídia garantam que seu processamento de tempo-diferenciado recebe acesso priorizado aos recursos da CPU.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Serviço do Agendador de classes de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80656276af30495c084d0964534a04e11896bcd2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930126"
---
# <a name="multimedia-class-scheduler-service"></a>Serviço do Agendador de classes de multimídia

O serviço do Agendador de classes de multimídia (MMCSS) permite que os aplicativos multimídia garantam que seu processamento de tempo-diferenciado recebe acesso priorizado aos recursos da CPU. Esse serviço permite que aplicativos multimídia utilizem o máximo possível da CPU sem negar recursos de CPU a aplicativos de prioridade mais baixa.

O MMCSS usa as informações armazenadas no registro para identificar as tarefas com suporte e determinar a prioridade relativa dos threads que executam essas tarefas. Cada thread que está executando o trabalho relacionado a uma tarefa específica chama a função [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) ou [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) para informar ao MMCSS que ele está trabalhando nessa tarefa.

Para obter um exemplo de um programa que usa o MMCSS, consulte [fluxos de modo exclusivo](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 e Windows XP:** O MMCSS não está disponível.

## <a name="registry-settings"></a>Configurações do Registro

As configurações do MMCSS são armazenadas na seguinte chave do registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ multimídia \\ SystemProfile**

Essa chave contém um valor **reg \_ DWORD** chamado **SystemResponsiveness** que determina a porcentagem de recursos de CPU que devem ser garantidos para tarefas de baixa prioridade. Por exemplo, se esse valor for 20, 20% dos recursos da CPU serão reservados para tarefas de baixa prioridade. Observe que os valores que não são divisíveis igualmente por 10 são arredondados para o múltiplo mais próximo de 10. Um valor de 0 também é tratado como 10.

A chave também contém uma subchave chamada **tarefas** que contém a lista de tarefas. Por padrão, o Windows oferece suporte às seguintes tarefas:

-   **Sonoro**
-   **Captura**
-   **Distribuição**
-   **Jogos**
-   **Reprodução**
-   **Áudio pro**
-   **Gerenciador de janelas**

Os OEMs podem adicionar outras tarefas conforme necessário.

Cada chave de tarefa contém o seguinte conjunto de valores que representam as características a serem aplicadas aos threads associados à tarefa.

| Valor                   | Formatar         | Valores possíveis                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Afinidade**            | **REG \_ DWORD** | Um bitmask que indica a afinidade do processador. Tanto 0x00 quanto 0xFFFFFFFF indicam que a afinidade do processador não é usada.                                                                                                                                                                                                                                                 |
| **Somente segundo plano**     | **REG \_ sz**    | Indica se esta é uma tarefa em segundo plano (sem interface do usuário). Os threads de uma tarefa em segundo plano não são alterados devido a uma alteração no foco da janela. Esse valor pode ser definido como true ou false.                                                                                                                                                                            |
| **BackgroundPriority**  | **REG \_ DWORD** | A prioridade do plano de fundo. O intervalo de valores é 1-8.                                                                                                                                                                                                                                                                                                                    |
| **Taxa do relógio**          | **REG \_ DWORD** | Uma dica usada pelo MMCSS para determinar a granularidade do agendamento de recursos do processador. **Windows Server 2008 e Windows Vista:** A taxa de relógio máxima garantida que o sistema usará se um thread ingressar nessa tarefa, em intervalos de 100 a nanossegundos. A partir do Windows 7 e do Windows Server 2008 R2, essa garantia foi removida para reduzir o consumo de energia do sistema.<br/> |
| **Prioridade da GPU**        | **REG \_ DWORD** | A prioridade da GPU. O intervalo de valores é 0-31. Essa prioridade ainda não foi usada.                                                                                                                                                                                                                                                                                           |
| **Prioridade**            | **REG \_ DWORD** | A prioridade da tarefa. O intervalo de valores é 1 (baixo) a 8 (alto). Para tarefas com uma **categoria de agendamento** alta, esse valor é sempre tratado como 2.<br/>                                                                                                                                                                                                           |
| **Categoria de agendamento** | **REG \_ sz**    | A categoria de agendamento. Esse valor pode ser definido como alto, médio ou baixo.                                                                                                                                                                                                                                                                                                 |
| **Prioridade SFIO**       | **REG \_ sz**    | A prioridade de e/s agendada. Esse valor pode ser definido como ocioso, baixo, normal ou alto. Este valor não é usado.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Para conservar energia, os aplicativos não devem definir a resolução do temporizador de todo o sistema para um valor pequeno, a menos que seja absolutamente necessário. Para obter mais informações, consulte [desempenho](../win7devguide/performance.md) no [Guia de desenvolvedores do Windows 7](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Prioridades do thread

O MMCSS aumenta a prioridade dos threads que estão trabalhando em tarefas de multimídia de alta prioridade.

O MMCSS determina a prioridade de um thread usando os seguintes fatores:

-   A prioridade base da tarefa.
-   O parâmetro *Priority* da função [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority) .
-   Se o aplicativo está em primeiro plano.
-   Quanto tempo de CPU está sendo consumido pelos threads em cada categoria.

O MMCSS define a prioridade dos threads de cliente, dependendo de sua categoria de agendamento.

| Categoria | Prioridade | Descrição                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Alto     | 23-26    | Esses threads são executados em uma prioridade de thread inferior a apenas determinadas tarefas em nível de sistema. Essa categoria foi projetada para tarefas de Pro Audio. |
| Médio   | 16-22    | Esses threads fazem parte do aplicativo que está em primeiro plano.                                                                      |
| Baixo      | 8-15     | Essa categoria contém o restante dos threads. Eles têm garantia de um percentual mínimo dos recursos da CPU, se necessário.           |
|          | 1-7      | Esses threads usaram sua cota de recursos de CPU. Eles poderão continuar sendo executados se nenhum thread de baixa prioridade estiver pronto para execução.                |



 

 

 
