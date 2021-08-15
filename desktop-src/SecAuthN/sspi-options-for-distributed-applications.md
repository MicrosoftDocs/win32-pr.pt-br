---
description: Opções de SSPI para aplicativos distribuídos
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opções de SSPI para aplicativos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfeef5cb52494c50b8b16911f70de238a7a86493297ec59bf6d46637810bf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916786"
---
# <a name="sspi-options-for-distributed-applications"></a>Opções de SSPI para aplicativos distribuídos

Os desenvolvedores têm muitas opções para a criação de aplicativos distribuídos. A [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) fornece uma camada de abstração entre protocolos de nível de aplicativo e protocolos de [*segurança*](../secgloss/s-gly.md). Os aplicativos podem aproveitar os protocolos de segurança SSPI de várias maneiras:

-   Chame as rotinas SSPI diretamente (para aplicativos tradicionais baseados em soquete).

    As rotinas usam mensagens de solicitação/resposta para implementar o [*protocolo de aplicativo*](../secgloss/a-gly.md) que transporta dados do SSPI relacionados à segurança.

-   Use COM para chamar opções de segurança que são implementadas usando RPC autenticado e SSPI em níveis inferiores.

    Esses aplicativos não chamam funções SSPI diretamente.

-   use o [Windows sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) com a interface do winsock estendida para permitir que os provedores de transporte usem recursos de segurança.

    Essa abordagem integra o SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) à pilha de rede e fornece serviços de segurança e transporte por meio de uma interface comum.

-   Use o [Windows internet Extensions API](../wininet/portal.md) (WinInet) e uma interface projetada para oferecer suporte a protocolos de segurança da internet, como o protocolo [*protocolo SSL*](../secgloss/s-gly.md) (SSL).

    Os aplicativos usam a interface SSPI para o provedor de segurança do [canal seguro](secure-channel.md) (Schannel) para implementar a segurança do Wininet. O Schannel é a implementação do SSL da Microsoft.

Várias funções SSPI retornam carimbos de data/hora que representam o período de vida de vários objetos. Os [*pacotes de segurança*](../secgloss/s-gly.md) podem manter o tempo e fornecer carimbos de data/hora de maneiras diferentes, mas usar a hora local simplifica o trabalho dos aplicativos que usam funções SSPI.

 

 
