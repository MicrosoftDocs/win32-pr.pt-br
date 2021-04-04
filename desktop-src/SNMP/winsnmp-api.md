---
title: API WinSNMP
description: A interface de programação de aplicativo SNMP do Microsoft Windows (a API WinSNMP) versões 1.1 a e 2,0 permitem que você desenvolva aplicativos de gerenciamento de rede baseados em SNMP que são executados no ambiente do Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007883"
---
# <a name="winsnmp-api"></a>API WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

A interface de programação de aplicativo SNMP do Microsoft Windows (a API WinSNMP) versões 1.1 a e 2,0 permitem que você desenvolva aplicativos de gerenciamento de rede baseados em SNMP que são executados no ambiente do Windows. O SNMP (Simple Network Management Protocol) é um protocolo de solicitação-resposta que transfere informações de gerenciamento entre entidades de protocolo.

O WinSNMP foi desenvolvido em conjunto com a cooperação, a entrada e o suporte de várias empresas, associações e indivíduos.

A primeira parte desta visão geral fornece informações sobre o adendo do WinSNMP 2,0, as versões SNMP e uma lista das solicitações relevantes de comentários (RFCs). Ele também descreve o modelo WinSNMP e os componentes e recursos da implementação do Microsoft WinSNMP. Ele também fornece informações sobre conceitos de comunicações e gerenciamento de dados de que você precisa para programar no ambiente WinSNMP.

A segunda seção discute as funções WinSNMP e as seguintes tarefas de programação de WinSNMP relacionadas:

-   [Abrindo e fechando um aplicativo WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Abrindo e fechando uma sessão WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Gerenciando interceptações e notificações](managing-traps-and-notifications.md)
-   [Trabalhando com listas de associação de variáveis](working-with-variable-binding-lists.md)
-   [Trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md)
-   [Enviando mensagens SNMP](sending-snmp-messages.md)
-   [Recebendo mensagens SNMP](receiving-snmp-messages.md)
-   [Gerenciando identificadores de objeto](managing-object-identifiers.md)
-   [Liberando descritores de WinSNMP](freeing-winsnmp-descriptors.md)
-   [Definindo a entidade e o modo de tradução de contexto](setting-the-entity-and-context-translation-mode.md)
-   [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md)
-   [Escrevendo aplicativos WinSNMP com vários threads](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registrando um aplicativo de agente SNMP](registering-an-snmp-agent-application.md)

Você deve estar familiarizado com os conceitos básicos do SNMP e da programação do Windows antes de ler esta visão geral. Para obter mais informações sobre SNMP, consulte [protocolo de gerenciamento de rede simples](simple-network-management-protocol-snmp-.md) e as solicitações relevantes de comentários (RFCs) que são publicadas pela IETF (Internet Engineering Task Force).

 

 