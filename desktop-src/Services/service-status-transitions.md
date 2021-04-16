---
description: Um serviço é responsável por relatar alterações em seu estado para o SCM (Gerenciador de controle de serviço).
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transições de estado do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df7684b1ebc04aa1116b09a3ae4321f2552d7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556108"
---
# <a name="service-state-transitions"></a>Transições de estado do serviço

Um serviço é responsável por relatar alterações em seu estado para o SCM (Gerenciador de controle de serviço). Os programas de controle de serviço e o sistema podem descobrir o estado de um serviço somente do SCM, portanto, é importante que um serviço relate seu estado corretamente. Um serviço relata seu estado chamando a função [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com um ponteiro para uma estrutura de [**\_ status de serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) totalmente inicializada. O membro **dwCurrentState** da estrutura contém o estado do serviço a ser relatado.

O estado inicial de um serviço é serviço \_ interrompido. Quando o SCM inicia o serviço, ele define o estado do serviço como serviço de \_ início \_ pendente e chama a [](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) função de serviço de funções. Em seguida, o serviço conclui sua inicialização usando uma das técnicas descritas na [função Service-Main](service-servicemain-function.md). Depois que o serviço concluir sua inicialização e estiver pronto para começar a receber solicitações de controle, o serviço chamará [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para o serviço de relatório \_ em execução e especificará as solicitações de controle que o serviço está preparado para aceitar. A transição do início do serviço \_ \_ pendente para \_ o serviço em execução indica as ferramentas de monitoramento de serviço e SCM que o serviço iniciou com êxito. Se o serviço relatar um estado diferente do serviço \_ em execução, as ferramentas SCM ou monitoramento de serviço poderão marcar o serviço como tendo falhado ao iniciar.

O SCM envia apenas as solicitações de controle especificadas para o serviço (exceto para a \_ solicitação de interrogação de controle de serviço \_ , que é sempre enviada). Para obter uma lista das solicitações de controle que um serviço pode aceitar, consulte o membro **dwControlsAccepted** da estrutura de [**\_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Para obter informações sobre como registrar-se para receber eventos de dispositivo, consulte a função [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

O estado do serviço normalmente muda como resultado do tratamento de uma solicitação de controle. As solicitações de controle que fazem com que o estado do serviço mudem incluem \_ interrupção do controle \_ de serviço, pausa de controle de serviço \_ \_ e continuação do \_ controle \_ de serviço. Se o serviço precisar fazer processamento longo para lidar com qualquer uma dessas solicitações, ele deverá criar um thread secundário para executar o processamento longo e relatar o estado pendente correspondente ao SCM. (Para obter um melhor desempenho no Windows Vista e em versões posteriores do Windows, o serviço deve usar um thread de trabalho de um [pool de threads](/windows/desktop/ProcThread/thread-pools) para essa finalidade.) O serviço deve reportar a transição de estado concluído quando o processamento longo for concluído. Para obter mais informações sobre como lidar com solicitações de controle, consulte [função do manipulador de controle de serviço](service-control-handler-function.md).

Somente determinadas transições de estado de serviço são válidas. O diagrama a seguir mostra as transições válidas.

![transições de status de serviço válidas](images/service-status-transitions.png)

O estado do serviço relatado para o SCM determina como o SCM interage com o serviço. Por exemplo, se um serviço de relatórios de serviço \_ parar \_ pendente, o SCM não transmitirá mais solicitações de controle para o serviço, pois esse estado indica que o serviço está sendo desligado. O próximo estado relatado pelo serviço deve ser serviço \_ interrompido porque esse é o único estado válido após a interrupção do serviço ser \_ \_ pendente. No entanto, se um serviço reportar uma transição que não seja válida, o SCM não falhará na chamada.

O diagrama a seguir mostra as transições de estado de serviço em mais detalhes, incluindo as solicitações de controle iniciadas por um programa de controle de serviço (o cliente de serviço) e as chamadas [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) que um serviço faz para relatar alterações de estado para o SCM. Como mencionado anteriormente, o SCM envia apenas as solicitações de controle que o serviço especificou que ele aceitará, de modo que um serviço pode não receber todas as solicitações mostradas no diagrama.

![transições de status de serviço em detalhes ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**Falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
