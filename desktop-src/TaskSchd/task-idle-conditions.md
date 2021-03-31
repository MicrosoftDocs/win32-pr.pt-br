---
title: Condições de ociosidade da tarefa
description: Uma tarefa pode ser tratada de várias maneiras quando o computador entra em um estado ocioso. Isso inclui definir um gatilho ocioso ou definir as condições ociosas para quando a tarefa for iniciada.
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- condições de ociosidade Agendador de Tarefas
- condições de ociosidade Agendador de Tarefas, discussão
- Criando gatilhos ociosos Agendador de Tarefas
- gatilhos ociosos Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/19/2020
ms.locfileid: "103642941"
---
# <a name="task-idle-conditions"></a>Condições de ociosidade da tarefa

Uma tarefa pode ser tratada de várias maneiras quando o computador entra em um estado ocioso. Isso inclui definir um gatilho ocioso ou definir as condições ociosas para quando a tarefa for iniciada.

## <a name="detecting-the-idle-state"></a>Detectando o estado ocioso

No Windows 7, a Agendador de Tarefas verifica se o computador está em um estado ocioso a cada 15 minutos. Agendador de Tarefas verifica se há um estado ocioso usando dois critérios: ausência do usuário e falta de consumo de recursos. O usuário será considerado ausente se não houver nenhuma entrada de teclado ou mouse durante esse período de tempo. O computador será considerado ocioso se todos os processadores e todos os discos estiverem ociosos por mais de 90% do último intervalo de detecção. (Uma exceção seria para qualquer aplicativo de tipo de apresentação que define o ES \_ Exibir \_ sinalizador necessário. Esse sinalizador força a agenda de tarefas a não considerar o sistema como ocioso, independentemente da atividade do usuário ou do consumo de recursos.)

No Windows 7, Agendador de Tarefas considera um processador como ocioso mesmo quando os threads de baixa prioridade (prioridade de thread < normal) são executados.

No Windows 7, quando o Agendador de Tarefas detecta que o computador está ocioso, o serviço aguarda apenas a entrada do usuário para marcar o final do estado ocioso.

No Windows 8, Agendador de Tarefas executa as mesmas verificações gerais de ausência de usuário e consumo de recursos. No entanto, Agendador de Tarefas se baseia no subsistema de energia do sistema operacional para detectar a presença do usuário. Por padrão, o usuário é considerado ausente após quatro minutos sem nenhuma entrada de teclado ou mouse. O tempo de verificação de consumo de recursos é reduzido para intervalos de 10 minutos quando o usuário está presente. Quando o usuário estiver ausente, o tempo de verificação será reduzido para intervalos de 30 segundos. Agendador de Tarefas faz verificações adicionais de consumo de recursos para os seguintes eventos:

-   Estado de presença do usuário alterado
-   Fonte de energia CA/DC alterada
-   Nível de bateria alterado (somente quando nas baterias)

Quando qualquer um dos eventos acima ocorre, Agendador de Tarefas testa o computador quanto à inatividade desde a última hora de verificação. Na prática, isso significa que Agendador de Tarefas pode declarar o sistema como ocioso imediatamente após a ausência do usuário ser detectada, se as outras condições tiverem sido atendidas desde a última hora de verificação.

No Windows 8, os limites de CPU e e/s são definidos como 80%.

Ao detectar o estado ocioso no Windows 8 Server, Agendador de Tarefas não leva a presença do usuário nem a ausência em conta. Para marcar o final do estado ocioso, Agendador de Tarefas revisa o consumo de recursos uma vez em 90 minutos.

## <a name="defining-an-idle-trigger"></a>Definindo um gatilho ocioso

Uma tarefa pode ser iniciada quando o computador entra em um estado ocioso definindo um gatilho ocioso.

Um gatilho ocioso só disparará uma ação de tarefa se o computador entrar em um estado ocioso após o limite inicial do gatilho.

Um aplicativo pode definir um gatilho ocioso usando a interface [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Se estiver lendo ou gravando XML, o gatilho de ociosidade será especificado pelo elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

## <a name="task-settings-for-idle-conditions"></a>Configurações de tarefa para condições ociosas

As configurações de tarefa podem ser usadas para definir como a Agendador de Tarefas trata a tarefa quando o computador entra em um estado ocioso.

As ilustrações a seguir fornecem três possíveis linhas do tempo que mostram como essas diferentes condições ociosas se relacionam entre si. Lembre-se de que as ilustrações iniciam quando o gatilho de tarefa é ativado ou quando a tarefa é iniciada sob demanda (sem solicitar a [ignorar as restrições de tarefa existentes](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)).

> [!NOTE]
> As configurações de *duração* e *WaitTimeout* são preteridas. Eles ainda estão presentes na interface do usuário Agendador de Tarefas, e seus métodos de interface ainda podem retornar valores válidos, mas não são mais usados.

![linha do tempo de condição ociosa](images/idle-conditions2.png)

A lista a seguir descreve as condições de ociosidade.
- Início de ociosidade: a hora em que o computador entra no estado ocioso.
- Fim de ociosidade: a hora em que o computador faz a transição para fora do estado ocioso. Lembre-se de que a quantidade de tempo que o computador está no estado ocioso é independente do tempo de duração ocioso descrito anteriormente.

A espera de ociosidade e a duração de ociosidade foram preteridas.
- Espera de ociosidade: a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de um estado ocioso depois que um gatilho de tarefa for ativado ou depois que a tarefa for iniciada sob demanda.
- Duração ociosa: a quantidade de tempo que você deseja que o computador fique ocioso antes de iniciar a tarefa.

Por exemplo, se uma tarefa for definida para iniciar somente se o computador estiver ocioso por 30 minutos e a tarefa aguardar o computador ficar ocioso por 10 minutos, a tarefa será iniciada em 5 minutos somente se o computador ficar ocioso por 25 minutos antes da hora em que o gatilho foi ativado. A tarefa não será iniciada se o computador entrar em um estado ocioso 5 minutos depois que o gatilho for ativado.

Por padrão, uma Propriedade Task [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) é definida como true, o que significa que o serviço de Agendador de tarefas não executará as tarefas disparadas por um gatilho ocioso (ou um gatilho com condições ociosas) quando um computador estiver sendo executado com energia da bateria. Você pode alterar esse comportamento definindo a propriedade **DisallowStartIfOnBatteries** como false.

Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) da interface [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) ([**IdleSettings**](idlesettings.md) para scripts) será ignorada.

Os aplicativos podem controlar as condições ociosas definindo as propriedades nas interfaces [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) e [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Se estiver lendo ou gravando XML, essas condições serão especificadas no elemento [**configurações**](taskschedulerschema-settings-tasktype-element.md) do esquema de Agendador de tarefas.

## <a name="cycling-idle-condition"></a>Condição de ociosidade do ciclo

Se o computador estiver alternando e saindo do estado ocioso, você poderá encerrar e reiniciar a tarefa usando as seguintes condições ociosas. Para encerrar e reiniciar uma tarefa, as propriedades e os elementos devem ser definidos como true:

-   Para encerrar a tarefa quando a condição ociosa terminar, defina a propriedade [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) ou o elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) como true.
-   Para reiniciar a tarefa quando o computador entrar na condição de ociosidade novamente, defina a propriedade [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) ou o elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) como true.
