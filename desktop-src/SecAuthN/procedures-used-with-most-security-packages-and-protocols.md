---
description: O modelo SSPI (Security Support Provider interface) fornece uma interface única para um aplicativo de transporte de cliente/servidor usando os vários pacotes de segurança disponíveis em um computador ou rede.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedimentos usados com a maioria dos pacotes de segurança e protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501589"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procedimentos usados com a maioria dos pacotes de segurança e protocolos

O modelo SSPI ( [*Security Support Provider interface*](../secgloss/s-gly.md) ) fornece uma interface única para um aplicativo de transporte de cliente/servidor usando os vários [*pacotes de segurança*](../secgloss/s-gly.md) disponíveis em um computador ou rede. O SSPI permite que um aplicativo use um pacote de segurança sem lidar com os [*protocolos de segurança*](../secgloss/s-gly.md) subjacentes do pacote. Ao mesmo tempo, o SSPI também permite que aplicativos sofisticados com reconhecimento de segurança aproveitem os recursos avançados de pacotes de segurança específicos.

Os aplicativos inicializam SSPI usando as seguintes etapas para proteger uma conexão de rede para a maioria dos pacotes de segurança:

-   [Usando SecBufferDesc e SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Inicializando SSPI](initializing-sspi.md)
-   [Estabelecendo uma conexão segura com autenticação](establishing-a-secure-connection-with-authentication.md)
-   [Garantindo a integridade da comunicação durante a troca de mensagens](ensuring-communication-integrity-during-message-exchange.md)
-   [Encerrando uma sessão SSPI](ending-an-sspi-session.md)

 

 
