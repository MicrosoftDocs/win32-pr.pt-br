---
description: O modelo SSPI (Interface do Provedor de Suporte de Segurança) fornece uma única interface para um aplicativo de transporte cliente/servidor usando os vários pacotes de segurança disponíveis em um computador ou rede.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedimentos usados com a maioria dos pacotes e protocolos de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611ecbf7f2a124ea9352a71c7197d298f30a43391e3692303fcd3f7bc533cc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920745"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procedimentos usados com a maioria dos pacotes e protocolos de segurança

O modelo SSPI [*(Interface*](../secgloss/s-gly.md) do Provedor de Suporte de Segurança) fornece [](../secgloss/s-gly.md) uma única interface para um aplicativo de transporte cliente/servidor usando os vários pacotes de segurança disponíveis em um computador ou rede. O SSPI permite que um aplicativo use um pacote de segurança sem lidar com os protocolos de [*segurança subjacentes*](../secgloss/s-gly.md) do pacote. Ao mesmo tempo, o SSPI também permite que aplicativos sofisticados e com segurança aproveitem os recursos avançados de pacotes de segurança específicos.

Os aplicativos inicializam o SSPI usando as seguintes etapas para proteger uma conexão de rede para a maioria dos pacotes de segurança:

-   [Usando SecBufferDesc e SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Inicializando o SSPI](initializing-sspi.md)
-   [Estabelecendo uma conexão segura com autenticação](establishing-a-secure-connection-with-authentication.md)
-   [Garantir a integridade da comunicação durante a Exchange](ensuring-communication-integrity-during-message-exchange.md)
-   [Encerrando uma sessão SSPI](ending-an-sspi-session.md)

 

 
