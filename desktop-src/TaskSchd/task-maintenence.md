---
title: Manutenção automática (Agendador de Tarefas)
description: A atividade de manutenção refere-se a um aplicativo ou processo que ajuda a manter a integridade e o desempenho de um computador Windows.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456383eeb75c3b29bf575357d4b17d5f8a66234b
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/19/2020
ms.locfileid: "104366862"
---
# <a name="automatic-maintenance"></a>Manutenção automática

A atividade de manutenção refere-se a um aplicativo ou processo que ajuda a manter a integridade e o desempenho de um computador Windows. A manutenção inclui manter o sistema operacional Windows (SO) e os aplicativos atualizados, verificar a segurança e executar verificações de malware. O gerenciamento automático do Windows (WAM) é um conjunto de aprimoramentos para a API Agendador de Tarefas que você pode usar para vincular seus aplicativos ao agendamento de manutenção do Windows. Especificamente, o WAM permite que você adicione atividades que exigem agendamento regular, mas que não têm requisitos de tempo exatos. Em vez disso, o WAM conta com o sistema operacional para escolher o tempo apropriado para ativar a tarefa ao longo do dia. O sistema escolhe esses horários com base no impacto mínimo sobre o usuário, o desempenho do PC e a eficiência energética.

## <a name="how-scheduled-maintenance-works"></a>Como funciona a manutenção agendada

Agendador de Tarefas tarefas de manutenção são tarefas oportunistas que são executadas quando o computador está ocioso e com energia CA. Um dos principais objetivos das tarefas de manutenção é minimizar o impacto para o PC agendando a manutenção somente quando o PC estiver conectado à energia AC e ocioso (ou seja, quando você não estiver usando ou tiver passado do computador). A ideia da manutenção hoje é que a máquina funcione com o mínimo de interrupções para o usuário. Portanto, a hora de manutenção em estilo antigo (falaremos mais sobre isso na seção **&mdash; ativação diária de manutenção automática** mais adiante neste tópico) foi aprimorada para aproveitar esses períodos ociosos. Embora a hora de manutenção ainda possa ser utilizada, a execução de manutenção oportunista é melhor para a integridade do sistema.

Sua tarefa poderá ficar sem interatividade se um computador não gastar muito tempo ocioso e em energia CA. Verifique se seu cenário ainda fornecerá valor para o usuário, mesmo se ele estiver atrasado. Se o usuário estiver usando ativamente o computador, o sistema adiará a manutenção até uma hora posterior. O sistema também suspende qualquer tarefa de manutenção em execução se o usuário retornar ao uso do PC.

O sistema reinicia uma tarefa de manutenção suspensa durante o próximo período ocioso; no entanto, o sistema não suspenderá nenhuma tarefa marcada como crítica. Em vez disso, o sistema permite que uma tarefa crítica seja concluída, independentemente da ação do usuário.

Devido à natureza do agendamento, algumas tarefas agendadas podem não ser concluídas: Talvez haja muitos eventos agendados para caber na janela de manutenção de uma hora ou talvez o computador simplesmente não esteja ligado. Nesses casos, você pode definir uma tarefa com um prazo final. Um prazo é definido como um período de tempo recorrente no qual o sistema deve executar a tarefa com êxito pelo menos uma vez.

Se uma tarefa perder um prazo, o Agendador de manutenção continuará tentando executar a tarefa durante a janela de manutenção. Além disso, o Agendador não se limitará ao limite de tempo normal de 1 hora. Em vez disso, o Agendador estende a duração da janela de manutenção a fim de concluir a tarefa atrasada.

Depois que o sistema concluir a tarefa (mesmo com um código de erro de falha), a tentativa será considerada bem-sucedida. Após uma tentativa bem-sucedida, o Agendador é redefinido para a agenda de manutenção regular e tentará a tarefa durante o próximo período.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Ativação diária de manutenção automática &mdash;

No Windows 7, uma tarefa de manutenção é executada exclusivamente durante a *hora de manutenção*, padronizando para 3 AM e configurável por meio de política de grupo. A máquina seria ativada em espera, executa tarefas de manutenção e volta para o modo de suspensão. Esta sessão diária foi limitada a uma duração máxima de 1 hora por tentativa. Isso permitiria que o sistema executasse a manutenção diariamente, começando às 3 AM por padrão. Observe que o usuário pode reagendar a hora em que a manutenção é disparada Configurando essas configurações.

Com o advento dos laptops e o foco pesado na vida útil da bateria, as máquinas não são mais configuradas para permitir a ativação S3 na maioria das circunstâncias e, geralmente, doze-to-S4 (hibernação) assim que possível, para economizar bateria. Em resposta a essas alterações, Agendador de Tarefas (> Win7) executa tarefas de manutenção sempre que elas estiverem vencidas e o computador estiver ocioso e em corrente alternada.

Essa configuração pode ser definida no painel de controle.

Abra sistema do **painel**  >  **de controle e**  >  **segurança de segurança e manutenção** manutenção  >  **automática**.

Com base em como seus computadores e suas tarefas estão configurados, o comportamento de ativação diária pode não ocorrer hoje como esperado devido a essa nova configuração. Você pode primeiro determinar se o computador é compatível com S3 ou o CS (conectado em espera).
Isso pode ser feito abrindo um prompt do Shell de energia com privilégios elevados e executando o comando a seguir.

```console
powercfg /a
```

Hora de manutenção, se a máquina estiver configurada corretamente, ainda funciona, mas se não estiver,
  - Verifique as configurações do BIOS para obter as configurações de ativação. 
  - Verifique se a opção permitir temporizador de ativação está habilitada nas opções de energia.
    Vá para **painel de controle**  >  **hardware e sons**  >  **Opções de energia**  >  **Editar configurações do plano**  >  **alterar configurações de energia avançadas** > clique em **suspensão**  >  **permitir temporizador de ativação**.
  - Verifique se a tarefa agendada está configurada com o seguinte.
      * MaintenanceSettings: a tarefa deve ser configurada com período, prazo final.
      * Habilitado: a tarefa deve ser habilitada.
      * WakeToRun: a tarefa deve ter permissão para ativar o computador.
  - Para o agendamento de ativações do CS, o computador deve ser compatível com AOAC.
  - Para o agendamento de ativações em computadores S3,
      * Verifique se o computador entrou em S3 em corrente alternada.
      * O sistema deve ter a **ativação habilitada** no política de grupo para manutenção.
 
A espera conectada é o estado do sistema que um sistema compatível com AOAC pode inserir.

Consulte as diferenças entre o modo de espera moderno e S3 no tópico [moderno em espera vs S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Definindo uma tarefa de manutenção automática

Você pode converter qualquer tarefa de Agendador de Tarefas em uma tarefa de manutenção. Para fazer isso, você deve confirmar que seu aplicativo pode ser suspenso. Em seguida, você deve estender a definição de tarefa com os novos elementos [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) e [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md) .

A principal preocupação com a criação de uma tarefa de manutenção é garantir que o sistema possa suspender e reiniciar a tarefa. O sistema provavelmente suspenderá uma tarefa de manutenção várias vezes; Portanto, você precisa garantir que seu aplicativo seja capaz de salvar seu próprio Estado e, em seguida, retomar em um horário arbitrário. Isso garante que o sistema não execute a mesma parte de sua tarefa repetidamente.

Depois de garantir que seu aplicativo pode ser suspenso e retomado normalmente, você pode usar os elementos **MaintenanceSettings** e **AllowStartOnDemand** para definir o agendamento. **MaintenanceSettings** é definido de acordo com o período, o prazo e o exclusividade.

-   O **período** é obrigatório e define a frequência com que a tarefa deve ocorrer. Normalmente, isso é definido em termos de um ciclo de vários dias, como "uma vez a cada 5 dias". Um período deve ser de pelo menos um dia, o que significa que não é possível agendar uma tarefa para ocorrer várias vezes em um dia.
-   O **prazo** é opcional e define por quanto tempo o Agendador pode falhar para concluir a tarefa antes de notificar o usuário ou executar a manutenção de emergência. O prazo final deve ser maior do que o período, o que significa que o sistema deve ter a oportunidade de tentar a tarefa pelo menos uma vez antes de notificar o usuário.
-   Além disso, uma tarefa de manutenção pode, opcionalmente, ser definida como *exclusiva*. Uma tarefa exclusiva é executada separadamente de outras tarefas de manutenção. Normalmente, uma tarefa exclusiva é aquela que usa um grande número de recursos, como uma grande quantidade de tempo de CPU ou acesso exclusivo a um banco de dados. O sistema conclui todas as tarefas de manutenção não exclusivas antes de iniciar uma tarefa exclusiva. Portanto, você deve declarar uma tarefa somente como exclusiva quando necessário.

Por outro lado, **AllowStartOnDemand** simplesmente indica que o sistema ou o usuário pode iniciar a tarefa a qualquer momento. Isso permite que o sistema inicie a tarefa durante a manutenção regular. Caso contrário, você precisaria definir um gatilho exclusivo para a tarefa.
