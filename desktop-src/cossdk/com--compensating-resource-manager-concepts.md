---
description: Você pode usar o CRM (Gerenciador de recursos de compensação COM+) para integrar facilmente e rapidamente recursos de aplicativos com transações do Microsoft Coordenador de Transações Distribuídas (DTC).
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Conceitos do Gerenciador de recursos de compensação COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920340"
---
# <a name="com-compensating-resource-manager-concepts"></a>Conceitos do Gerenciador de recursos de compensação COM+

Você pode usar o CRM (Gerenciador de recursos de compensação COM+) para integrar facilmente e rapidamente recursos de aplicativos com transações do Microsoft Coordenador de Transações Distribuídas (DTC). Os recursos do aplicativo podem votar no resultado de uma transação e podem receber a notificação final de seu resultado. Um log durável é gerado para que os recursos do aplicativo possam gravar registros que sobrevivem a falhas e o CRM recupera esse arquivo de log quando o aplicativo é reiniciado.

Um CRM consiste nos dois componentes a seguir:

-   CRM Worker. Esse componente executa o trabalho principal do CRM específico e implementa uma interface específica para a tarefa que precisa ser executada. A infraestrutura do CRM fornece uma interface para o trabalhador do CRM por meio da qual o trabalhador do CRM pode gravar registros em um arquivo de log durável no disco. O trabalho do CRM deve gravar registros no log e torná-los duráveis antes de executar seu trabalho para que, se ocorrer uma falha, a recuperação possa ocorrer corretamente. O trabalhador do CRM sempre requer uma transação.
-   Compensador de CRM. Esse componente é criado pela infraestrutura do CRM na conclusão da transação. Ele implementa uma interface definida pela qual a infra-estrutura de CRM pode passar notificações de conclusão de transação e os registros de log que foram gravados anteriormente pelo trabalhador do CRM.

Um CRM do COM+ fornece atomicidade com notificações transacionais e durabilidade com o log do CRM, mas não fornece isolamento de recursos. Em um ambiente multithread, é responsabilidade do desenvolvedor de CRM garantir que o acesso aos recursos, seja por vários trabalhadores do CRM ou aplicativos externos, seja serializado durante uma transação.

Depois que a transação tiver passado para a fase de preparação, o compensador de CRM e os funcionários do CRM poderão ser executados simultaneamente. É possível que o componente de trabalho do CRM de uma nova transação fique ativo enquanto o compensador de CRM de uma transação anterior ainda está processando a transação anterior.

Durante as falhas antes da recuperação do aplicativo do servidor do CRM, uma transação interrompida deve ser considerada ativa e não concluída. Não deve ser possível que os processos externos acessem os recursos que estavam sendo alterados por essa transação específica antes da recuperação do processo do servidor do CRM.

O CRM define três tipos de interface para as funções básicas do CRM:

-   O [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) é implementado no administrador do CRM e é usado pelo trabalhador do CRM para gravar registros de log no log. Ele também pode ser usado pelo compensador de CRM.
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) e [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) são implementados no compensador de CRM. Essas interfaces são usadas para fornecer notificações de resultado da transação e seus registros de log associados ao compensador de CRM. Normalmente, o compensador de CRM implementa apenas uma dessas interfaces, dependendo se ela exigiu registros de log estruturados ou não estruturados. Os *registros de log estruturados* são aqueles que são criados como uma coleção de variantes e normalmente são usados pelo Microsoft Visual Basic. Os *registros de log não estruturados* são apenas um buffer de bytes e normalmente são usados pelo Microsoft Visual C++. Um compensador de CRM pode implementar ambas as interfaces compensadoras; no entanto, apenas um de cada vez é usado para entregar registros de log.
-   As interfaces de monitoramento do CRM do COM+ são usadas para monitorar o CRMs em um aplicativo de servidor específico. Para obter informações detalhadas sobre as interfaces de monitoramento, consulte [interfaces de monitoramento do com+ CRM](com--crm-monitoring-interfaces.md).

Os tópicos a seguir nesta seção fornecem mais detalhes sobre o serviço CRM do COM+:

-   [Considerações de segurança do CRM do COM+](com--crm-security-considerations.md)
-   [Processo operacional de CRM do COM+](com--crm-operating-process.md)
-   [Inicialização e recuperação do CRM do COM+](com--crm-startup-and-recovery.md)
-   [Usando o CRM do COM+ em um ambiente de cluster](using-the-com--crm-in-a-cluster-environment.md)
-   [Tratamento de erros no CRM COM+](error-handling-in-the-com--crm.md)
-   [Configurações do registro do CRM do COM+](com--crm-registry-settings.md)
-   [Solucionando problemas do CRM do COM+](troubleshooting-the-com--crm.md)
-   [Sugestões de design para o desenvolvimento de um CRM COM+](design-suggestions-for-developing-a-com--crm.md)
-   [Interfaces de monitoramento do COM+ CRM](com--crm-monitoring-interfaces.md)
-   [Interfaces do CRM COM+](com--crm-interfaces.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



