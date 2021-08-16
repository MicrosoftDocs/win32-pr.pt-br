---
description: Processo operacional do COM+ CRM
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Processo operacional do COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308125"
---
# <a name="com-crm-operating-process"></a>Processo operacional do COM+ CRM

Em operação normal, um componente de aplicativo em execução em um processo de aplicativo de servidor usaria um CRM COM+ criando um trabalho crm. O trabalho crm implementa uma interface COM específica para a tarefa que ele foi projetado para executar. O componente do aplicativo deve estar em execução em uma transação para que o trabalho do CRM herde a transação do componente do aplicativo. Os trabalhadores do CRM sempre exigem uma transação.

Para acessar o COM+ CRM, o trabalho do CRM primeiro obtém a interface [**ICrmLogControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) que permite que o trabalho do CRM escreva registros no log durável. O trabalho do CRM obtém essa interface criando um componente de administrativo do CRM.

Em seguida, o trabalhador do CRM deve dizer ao funcionário do CRM o nome do compensador de CRM que deseja usar. Ele faz isso chamando o [**método ICrmLogControl::RegisterCompensator.**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) Depois que esse método é chamado, o compensador de CRM é criado pela infraestrutura crm quando a transação é concluída.

Depois que o trabalho crm registrou seu compensador crm, ele pode gravar registros no log crm usando [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). O trabalho do CRM deve *escrever com antecedência;* ou seja, ele deve gravar um registro no log que descreve uma ação antes de realmente executar a ação, caso ocorra uma falha imediatamente após a conclusão da ação. Sem esses registros de log de gravação antecipada, não há como corrigir a ação.

Além disso, escrever com antecedência significa que o Compensador de CRM, que é o componente que recebe os registros de log na recuperação, deve lidar com o caso em que os registros de log foram gravados, mas a ação não ocorreu de fato. As ações do compensador de CRM devem *ser idempotentes;* ou seja, eles devem ser capazes de serem executados mais de uma vez, mas devem levar ao mesmo resultado. Por exemplo, definir um saldo de conta com o valor de US$ 100 é uma ação idempotente; adicionar US$ 100 ao saldo da conta não é.

A [**interface ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) fornece os dois métodos a seguir para escrever registros de log:

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) é usado para gravar um registro de log estruturado criado como uma coleção de Variantes. Ele é usado principalmente ao desenvolver CRMs no Microsoft Visual Basic.
-   [**WriteLogRecord é**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) usado para gravar um registro de log não estruturado como BLOBs de bytes. Ele é usado principalmente ao desenvolver CRMs em Microsoft Visual C++. Como as estruturas de registro em C geralmente são feitas de um conjunto de headers e campos que podem ser dispersos na memória, o método **WriteLogRecord** implementa uma funcionalidade de coleta que reduz a cópia de dados.

> [!Note]  
> Você não deve os tipos de ponteiro de usuário em estruturas de dados em um registro de log. Os ponteiros não são mais válidos durante a fase de recuperação porque o Compensator do CRM é executado em um processo diferente do trabalho do CRM que escreveu o registro de log. Incluir tipos de ponteiro em um registro de log pode fazer com que um aplicativo falha ou se corrompa durante a recuperação.

 

Ambos os métodos de gravação gravam um registro de log no disco, mas não garantem a durabilidade do registro. Embora permitir que gravações lentas se acumule antes de forçar o disco a melhorar o desempenho, você pode usar o método [**ICrmLogControl::ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) para garantir que todas as gravações feitas pelo CRM sejam duráveis no disco, o que é importante para a recuperação de falhas.

Quando o trabalho do CRM terminar de escrever e forçar registros no log, ele deverá liberar [**ICrmLogControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) Quando a transação é concluída (normalmente devido ao componente de aplicativo que chama [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)), a infraestrutura crm cria o componente compensador crm, que implementa a interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) ou a interface [**ICrmCompensatorVariants.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) Essas interfaces são usadas para passar os registros não estruturados (Visual C++) ou estruturados (Visual Basic) para o Compensador do CRM juntamente com as notificações de resultado da transação.

O Compensador de CRM é notificado pela primeira vez sobre a fase de preparação da conclusão da transação e pode votar em sim ou não na solicitação de preparação. Se o compensador de CRM votar em não, ele não receberá nenhuma notificação de anulação adicional. Se ele votar em sim para a solicitação de preparação, ele receberá as notificações de confirmação ou anulação. No caso de uma anulação do cliente, nenhuma notificação de preparação é recebida, somente notificações de anulação. O Compensador de CRM deve estar preparado para lidar com todos esses casos e também deve lidar com o caso em que nenhum registro de log foi gravado com êxito pelo trabalho do CRM. O Compensador de CRM não deve presumir que a mesma instância do CRM Compensator receberá as notificações da fase 1 (preparação) e da fase 2 (confirmação ou anulação), pois elas podem ser interrompidas pela recuperação.

Normalmente, um Compensador de CRM usa a notificação de anulação para reverter a ação que foi executada pelo trabalho do CRM. O trabalho do CRM pode deixar algum estado disponível caso precise reverter sua ação. Esse estado pode estar totalmente contido nos registros de log e, caso não seja, o Compensador de CRM precisará limpar esse estado se a transação for confirmada. Esse é o motivo pelo qual o Compensador de CRM recebe a notificação de confirmação. O CRM Compensator não é executado em uma transação DTC.

O Compensador de CRM pode registrar novos registros se necessário usando [**ICrmLogControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)que ele recebe conforme ele é criado. O crm worker e o CRM Compensator também podem esquecer o último registro de log que eles escreveram, o que pode ser necessário para evitar a recuperação desnecessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de Resource Manager com+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Inicialização e recuperação do COM+ CRM](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



