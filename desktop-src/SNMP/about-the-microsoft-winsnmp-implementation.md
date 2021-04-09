---
title: Sobre a implementação do Microsoft WinSNMP
description: A implementação do Microsoft WinSNMP está em conformidade com o WinSNMP versão 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915865"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Sobre a implementação do Microsoft WinSNMP

A implementação do Microsoft WinSNMP está em conformidade com o WinSNMP versão 2,0. Ele dá suporte a todas as funções e operações definidas na especificação do WinSNMP versão 1.1 a e no adendo do WinSNMP versão 2,0. A implementação fornece os seguintes serviços para aplicativos de WinSNMP:

-   Gerencia comunicações de e para entidades de gerenciamento. A entidade pode residir no computador local ou estar conectada por meio de uma rede local ou de longa distância, ou a Internet. Para obter mais informações, consulte [níveis de suporte a SNMP](levels-of-snmp-support.md).
-   Oculta os detalhes do protocolo SNMP, da notação de sintaxe abstrata um (ASN. 1) e as regras de codificação básica (BER) para descrever a sintaxe de transferência.
-   Verifica a exatidão de PDUs e rejeita PDUs inválidas. Para obter mais informações, consulte [trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).
-   Transforma os tipos de PDU do SNMPv2C quando necessário de acordo com as RFCs relevantes.
-   Converte as armadilhas de SNMPv1 de um agente SNMPv1 em interceptações de SNMPv2C de acordo com a RFC 1908, "coexistência entre a versão 1 e a versão 2 da estrutura de gerenciamento de rede padrão da Internet". Para obter mais informações, consulte [convertendo interceptações de SNMPv1 para SNMPv2c](translating-traps-from-snmpv1-to-snmpv2c.md).
-   Dá suporte à política de retransmissão do aplicativo e fornece suporte à execução de retransmissão. Para obter mais informações, consulte [o banco de dados WinSNMP](the-winsnmp-database.md) e [sobre a retransmissão](about-retransmission.md).
-   Fornece suporte à tradução de contexto e entidade para o aplicativo. Para obter mais informações, consulte [o banco de dados WinSNMP](the-winsnmp-database.md) e [definindo o modo de tradução de entidade e contexto](setting-the-entity-and-context-translation-mode.md).

Para obter informações adicionais sobre a relação entre um aplicativo WinSNMP e a implementação, consulte [conceitos de gerenciamento de dados de WinSNMP](winsnmp-data-management-concepts.md) e sessões de [WinSNMP](winsnmp-sessions.md).

 

 




