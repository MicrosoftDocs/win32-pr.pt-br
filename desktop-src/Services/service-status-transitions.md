---
description: Um serviço é responsável por relatar alterações em seu estado para o SCM (gerenciador de controle de serviço).
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transições de estado do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039caf68ee7d9da93e86e1760e49df87667da8c16eb5ca6693cfdc7db7def2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967301"
---
# <a name="service-state-transitions"></a>Transições de estado do serviço

Um serviço é responsável por relatar alterações em seu estado para o SCM (gerenciador de controle de serviço). Os programas de controle de serviço e o sistema podem descobrir o estado de um serviço somente do SCM, portanto, é importante que um serviço reporte seu estado corretamente. Um serviço relata seu estado chamando a [**função SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com um ponteiro para uma estrutura [**SERVICE STATUS totalmente \_ inicializada.**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) O **membro dwCurrentState** da estrutura contém o estado do serviço a ser relatado.

O estado inicial de um serviço é SERVICE \_ STOPPED. Quando o SCM inicia o serviço, ele define o estado do serviço como SERVICE START PENDING e chama a função \_ \_ [*ServiceMain do*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) serviço. Em seguida, o serviço conclui sua inicialização usando uma das técnicas descritas em [Função ServiceMain](service-servicemain-function.md). Depois que o serviço concluir sua inicialização e estiver pronto para começar a receber solicitações de controle, o serviço chamará [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para relatar SERVICE RUNNING e especificar as solicitações de controle que o serviço está preparado para \_ aceitar. A transição de SERVICE START PENDING para SERVICE RUNNING indica para as ferramentas de monitoramento de serviço e SCM que o \_ serviço foi iniciado com \_ \_ êxito. Se o serviço relata um estado diferente de SERVICE RUNNING, o SCM ou as ferramentas de monitoramento de serviço podem marcar o serviço como tendo \_ falhado ao iniciar.

O SCM envia apenas as solicitações de controle especificadas para o serviço (exceto para a solicitação DE \_ CONTROLE DE \_ SERVIÇO, QUE sempre é enviada). Para ver uma lista das solicitações de controle que um serviço pode aceitar, consulte **o membro dwControlsAccepted** da estrutura [**STATUS \_ DO**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) SERVIÇO. Para obter informações sobre como registrar-se para receber eventos de dispositivo, consulte [**a função RegisterDeviceNotification.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)

O estado do serviço normalmente muda como resultado do tratamento de uma solicitação de controle. As solicitações de controle que causam a alteração do estado do serviço incluem SERVICE \_ CONTROL \_ STOP, SERVICE \_ CONTROL PAUSE e SERVICE CONTROL \_ \_ \_ CONTINUE. Se o serviço tiver que realizar um processamento demorado para lidar com qualquer uma dessas solicitações, ele deverá criar um thread secundário para executar o processamento demorado e relatar o estado pendente correspondente ao SCM. (Para melhor desempenho no Windows Vista e versões posteriores do Windows, o serviço deve usar um thread de trabalho de um [pool de threads](/windows/desktop/ProcThread/thread-pools) para essa finalidade.) Em seguida, o serviço deve relatar a transição de estado concluída quando o processamento demorado for concluído. Para obter mais informações sobre como lidar com solicitações de controle, consulte [Função do manipulador de controle de serviço](service-control-handler-function.md).

Somente determinadas transições de estado de serviço são válidas. O diagrama a seguir mostra as transições válidas.

![transições de status de serviço válidas](images/service-status-transitions.png)

O estado do serviço relatado ao SCM determina como o SCM interage com o serviço. Por exemplo, se um serviço relata SERVICE STOP PENDING, o SCM não transmite mais solicitações de controle para o serviço porque esse estado indica que o serviço está \_ \_ sendo desligado. O próximo estado relatado pelo serviço deve ser SERVICE STOPPED porque esse é o único estado válido após \_ SERVICE \_ STOP \_ PENDING. No entanto, se um serviço relata uma transição que não é válida, o SCM não falha na chamada.

O diagrama a seguir mostra as transições de estado do serviço mais detalhadamente, incluindo as solicitações de controle iniciadas por um programa de controle de serviço (o cliente de serviço) e as chamadas [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) que um serviço faz para relatar alterações de estado para o SCM. Conforme mencionado anteriormente, o SCM envia apenas solicitações de controle que o serviço especificou que ele aceitará, portanto, um serviço pode não receber todas as solicitações mostradas no diagrama.

![transições de status do serviço em detalhes ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
