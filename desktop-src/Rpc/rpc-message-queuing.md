---
title: Enfileiramento de mensagens RPC
description: O MSMQ (enfileiramento de mensagens) permite que os usuários se comuniquem entre redes e sistemas, independentemente do estado atual dos aplicativos e sistemas de comunicação.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC de chamada de procedimento remoto, descrito, Enfileiramento de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c44296068087dc2fd4423dbb3294c3c7a417e8a983ec958c2ad765ff87ea81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018376"
---
# <a name="rpc-message-queuing"></a>Enfileiramento de mensagens RPC

O MSMQ (enfileiramento de mensagens) permite que os usuários se comuniquem entre redes e sistemas, independentemente do estado atual dos aplicativos e sistemas de comunicação. Os aplicativos enviam e recebem mensagens por meio de filas de mensagens que o MSMQ mantém. As filas de mensagens continuam a funcionar mesmo quando o aplicativo cliente ou servidor não está em execução. O enfileiramento de mensagens fornece:

-   **Mensagens assíncronas.** Com o sistema de mensagens assíncrono MSMQ, um aplicativo cliente pode enviar uma mensagem para um servidor e retornar imediatamente, mesmo que o computador de destino ou o programa do servidor não esteja respondendo.
-   **Entrega de mensagem garantida.** Quando um aplicativo envia uma mensagem por meio do MSMQ, a mensagem atingirá seu destino, mesmo se o aplicativo de destino não estiver em execução ao mesmo tempo ou se as redes e os sistemas estiverem offline.
-   **Roteamento e configuração dinâmica.** O MSMQ fornece roteamento flexível em redes heterogêneas. A configuração dessas redes pode ser alterada dinamicamente sem alterações importantes em sistemas e redes.
-   **Mensagens sem conexão.** Os aplicativos que usam o MSMQ não precisam configurar sessões diretas com aplicativos de destino.
-   [Segurança](security.md). o MSMQ fornece comunicação segura com base na segurança do Windows e na CryptoAPI (API de criptografia) para criptografia e assinaturas digitais.
-   **Mensagens priorizadas.** O MSMQ transfere mensagens entre redes com base na prioridade, permitindo uma comunicação mais rápida para aplicativos críticos.

O Microsoft RPC estende o modelo Open Software Foundation – equipamento de comunicações de dados (uso-DCE) para chamadas de procedimento remoto, permitindo que aplicativos distribuídos usem o MSMQ como um transporte e controlem muitos de seus recursos. Essa funcionalidade está disponível para aplicativos RPC convencionais e, por meio da interface **IRPCOptions** , para aplicativos com.

> [!Note]  
> o enfileiramento de mensagens RPC está disponível somente no Windows 2000. as versões posteriores do Windows não dão suporte ao enfileiramento de mensagens RPC.

 

Os tópicos a seguir fornecem uma visão geral do enfileiramento de mensagens:

-   [Visão geral da arquitetura dos serviços de enfileiramento de mensagens](overview-of-message-queuing-services-architecture.md)
-   [Propriedades da mensagem e da fila de mensagens](message-and-message-queue-properties.md)
-   [Usando o MSMQ como um transporte RPC](using-msmq-as-an-rpc-transport.md)
-   [Requisitos de sistema para RPC – \_ aplicativos de enfileiramento de mensagens](system-requirements-for-rpc-message-queuing-applications.md)
-   [Desenvolvendo aplicativos de enfileiramento RPC-Message](developing-rpc-message-queuing-applications.md)
-   [Serviços de segurança MSMQ](msmq-security-services.md)

 

 




