---
description: Processo operacional de CRM do COM+
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Processo operacional de CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308125"
---
# <a name="com-crm-operating-process"></a>Processo operacional de CRM do COM+

Em uma operação normal, um componente de aplicativo em execução em um processo de aplicativo de servidor usaria um CRM do COM+ criando um trabalho de CRM. O trabalhador do CRM implementa uma interface COM específica à tarefa que ele foi projetado para executar. O componente do aplicativo deve ser executado sob uma transação para que o trabalhador do CRM herde a transação do componente do aplicativo. Os trabalhadores do CRM sempre exigem uma transação.

Para acessar o CRM COM+, o trabalhador do CRM primeiro obtém a interface [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) , que permite que o trabalhador do CRM grave registros no log durável. O trabalhador do CRM obtém essa interface criando um componente do administrador do CRM.

Em seguida, o trabalhador do CRM deve informar ao administrador do CRM o nome do compensador de CRM que deseja usar. Ele faz isso chamando o método [**ICrmLogControl:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) . Depois que esse método é chamado, o compensador de CRM é criado pela infraestrutura do CRM quando a transação é concluída.

Depois que o trabalhador do CRM tiver registrado seu compensador de CRM, ele poderá gravar registros no log do CRM usando [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). O trabalhador do CRM deve fazer *write-ahead*; ou seja, ele deve gravar um registro no log que descreve uma ação antes de realmente executar a ação, caso uma falha ocorra imediatamente após a conclusão da ação. Sem esses registros de log write-ahead, não há nenhuma maneira de corrigir para a ação.

Além disso, write ahead significa que o compensador de CRM, que é o componente que recebe os registros de log na recuperação, deve lidar com o caso em que os registros de log foram gravados, mas a ação não realmente ocorre. As ações do compensador de CRM devem ser *idempotentes*; ou seja, eles devem ser capazes de serem executados mais de uma vez, mas devem levar ao mesmo resultado. Por exemplo, definir um saldo de conta com o valor de $100 é uma ação idempotente; Adicionar $100 ao saldo da conta não é.

A interface [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) fornece os dois métodos a seguir para gravar registros de log:

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) é usado para gravar um registro de log estruturado que é criado como uma coleção de variantes. Ele é usado principalmente para desenvolver CRMs no Microsoft Visual Basic.
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) é usado para gravar um registro de log não estruturado como BLOBs de bytes. Ele é usado principalmente para desenvolver CRMs em Microsoft Visual C++. Como as estruturas de registro em C geralmente são constituídas de um conjunto de cabeçalhos e campos que podem ser dispersos na memória, o método **WriteLogRecord** implementa um recurso de coleta que reduz a cópia de dados.

> [!Note]  
> Você não deve digitar os tipos de ponteiro do usuário em estruturas de dados em um registro de log. Os ponteiros não são mais válidos durante a fase de recuperação porque o compensador de CRM é executado em um processo diferente daquele do trabalhador do CRM que gravou o registro de log. A inclusão de tipos de ponteiro em um registro de log pode fazer com que um aplicativo falhe ou se corrompa durante a recuperação.

 

Esses dois métodos de gravação gravam um registro de log no disco, mas não garantem a durabilidade do registro. Embora permitir que as gravações lentas sejam acumuladas antes de forçar o disco possa melhorar o desempenho, você pode usar o método [**ICrmLogControl:: ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) em vez de garantir que todas as gravações feitas pelo CRM sejam duráveis em disco, o que é importante para a recuperação de falhas.

Quando o trabalhador do CRM é concluído com suas ações e concluiu a gravação e a força de registros no log, ele deve liberar [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). Quando a transação é concluída (normalmente devido ao componente de aplicativo chamando [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)), a infraestrutura de CRM cria o componente compensador de CRM, que implementa a interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) ou a interface [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) . essas interfaces são usadas para passar os registros não estruturados (Visual C++) ou estruturados (Visual Basic) para o compensador de CRM junto com as notificações de resultado da transação.

O compensador de CRM é notificado primeiro da fase de preparação da conclusão da transação e pode votar em Sim ou não na solicitação de preparação. Se o compensador de CRM não receber nenhuma outra notificação de anulação. Se ele tiver votos de Sim para a solicitação de preparação, ele receberá as notificações de confirmação ou anulação. No caso de uma anulação de cliente, nenhuma notificação de preparação é recebida, somente as notificações de anulação. O compensador de CRM deve estar preparado para lidar com todos esses casos e também deve lidar com o caso em que nenhum registro de log foi gravado com êxito pelo trabalhador do CRM. O compensador de CRM não deve assumir que a mesma instância de compensador de CRM receberá as notificações da fase 1 (preparação) e da fase 2 (confirmação ou anulação), pois elas podem ser interrompidas pela recuperação.

Normalmente, um compensador de CRM usa a notificação de anulação para reverter a ação que foi executada pelo trabalhador do CRM. O trabalhador do CRM pode deixar algum estado disponível caso precise reverter sua ação. Esse Estado pode estar totalmente contido nos registros de log e, se não for, o compensador de CRM precisará limpar esse Estado se a transação for confirmada. Esse é o motivo pelo qual o compensador de CRM recebe a notificação de confirmação. O compensador de CRM não é executado em uma transação DTC.

O compensador de CRM pode registrar novos registros, se necessário, usando [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol), que recebe à medida que ele é criado. O trabalho de CRM e o compensador de CRM também podem esquecer o último registro de log gravado, o que pode ser necessário para evitar a recuperação desnecessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Inicialização e recuperação do CRM do COM+](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



