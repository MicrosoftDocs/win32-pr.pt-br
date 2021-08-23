---
title: WinSNMP API
description: As versões 1.1a e 2.0 da Interface de Programação de Aplicativo SNMP do Microsoft Windows SNMP permitem que você desenvolva aplicativos de gerenciamento de rede baseados em SNMP que são executados no ambiente Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142979"
---
# <a name="winsnmp-api"></a>WinSNMP API

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, [Windows gerenciamento remoto,](/windows/desktop/WinRM/portal)que é a implementação da Microsoft do WS-Man.\]

As versões 1.1a e 2.0 da Interface de Programação de Aplicativo SNMP do Microsoft Windows SNMP permitem que você desenvolva aplicativos de gerenciamento de rede baseados em SNMP que são executados no ambiente Windows. O protocolo SNMP é um protocolo de solicitação-resposta que transfere informações de gerenciamento entre entidades de protocolo.

O WinSNMP foi desenvolvido em conjunto com a cooperação, a entrada e o suporte de várias empresas, associações e indivíduos.

A primeira parte desta visão geral fornece informações sobre o Adendo winSNMP 2.0, versões SNMP e uma lista das RFCs (Solicitações de Comentários) relevantes. Ele também descreve o modelo WinSNMP e os componentes e recursos da implementação do Microsoft WinSNMP. Ele também fornece informações sobre os conceitos de comunicação e gerenciamento de dados que você precisa programar no ambiente WinSNMP.

A segunda seção discute as funções WinSNMP e as seguintes tarefas de programação WinSNMP relacionadas:

-   [Abrindo e fechando um aplicativo WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Abrindo e fechando uma sessão winSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Gerenciando interceptações e notificações](managing-traps-and-notifications.md)
-   [Trabalhando com listas de associação de variáveis](working-with-variable-binding-lists.md)
-   [Trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md)
-   [Enviando mensagens SNMP](sending-snmp-messages.md)
-   [Recebendo mensagens SNMP](receiving-snmp-messages.md)
-   [Gerenciando identificadores de objeto](managing-object-identifiers.md)
-   [Liberando descritores WinSNMP](freeing-winsnmp-descriptors.md)
-   [Definindo a entidade e o modo de conversão de contexto](setting-the-entity-and-context-translation-mode.md)
-   [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md)
-   [Escrevendo aplicativos WinSNMP com vários threads](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registrando um aplicativo de agente SNMP](registering-an-snmp-agent-application.md)

Você deve estar familiarizado com os conceitos básicos de SNMP e programação Windows antes de ler esta visão geral. Para obter mais informações sobre [](simple-network-management-protocol-snmp-.md) o SNMP, consulte Protocolo de gerenciamento de rede simples e as RFCs (solicitações de comentários) relevantes publicadas pela IETF (Internet Engineering Task Force).

 

 