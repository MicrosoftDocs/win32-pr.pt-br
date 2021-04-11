---
title: Iniciar sequência
description: Etapas para iniciar o protocolo personalizado.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159403"
---
# <a name="start-sequence"></a>Iniciar sequência

Para iniciar seu provedor de protocolo, o serviço de Serviços de Área de Trabalho Remota:

-   Recupera o nome do ouvinte e o CLSID do seu objeto do Gerenciador de protocolos ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) do registro. Para obter mais informações, consulte [registrando o Gerenciador de protocolos](registering-the-custom-protocol.md).
-   Chama [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) para inicializar o Gerenciador de protocolo.
-   Cria um objeto Gerenciador de protocolos usando o CLSID. Mesmo se houver vários ouvintes registrados para o mesmo provedor de protocolo, o serviço criará apenas um objeto Gerenciador de protocolo.
-   Chama [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) para instruir o objeto Gerenciador de protocolos a criar um objeto de ouvinte [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) e retorná-lo ao serviço. O objeto Gerenciador de protocolo deve adicionar uma referência ao objeto de ouvinte antes de retorná-lo para o serviço. O serviço liberará o objeto quando o serviço for interrompido ou o ouvinte for excluído.
-   Chama [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) no objeto de ouvinte para que o ouvinte possa começar a escutar conexões de entrada.
-   Chama [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) para interromper a escuta do objeto de ouvinte.
-   Chama [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) para cancelar a inicialização do Gerenciador de protocolos.

O ouvinte cria um objeto [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) quando um cliente tenta se conectar. O objeto de ouvinte chama [**Onconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) para notificar o serviço de serviços de área de trabalho remota que um novo cliente está tentando se conectar ou reconectar e passa o objeto **IWRdsProtocolConnection** nessa chamada. O serviço de Serviços de Área de Trabalho Remota, por sua vez, retornará um objeto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) nessa chamada para que o protocolo possa se comunicar com o serviço serviços de área de trabalho remota, conforme necessário. O serviço adiciona uma referência ao objeto de retorno de chamada antes de retornar, e o protocolo deve liberar essa referência quando a conexão for fechada.

A ilustração a seguir mostra a interação entre os vários objetos durante a inicialização.

![RCM iniciar sequência](images/protocol-startsequence.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequência de chamada de método](method-call-sequence.md)
</dt> <dt>

[Sequência de conexão](connection-sequence.md)
</dt> </dl>

 

 




