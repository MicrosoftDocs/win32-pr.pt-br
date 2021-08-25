---
title: Convertendo interceptações de SNMPv1 para SNMPv2C
description: Quando a implementação do Microsoft WinSNMP recebe interceptações de uma entidade operando na estrutura SNMPv1, ela converte as interceptações no formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f70ddbdfb779f6b06f8ed26490c6fabd2421ae96f0006b4af5b7f1ab18f7d5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885856"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Convertendo interceptações de SNMPv1 para SNMPv2C

Quando a implementação do Microsoft WinSNMP recebe interceptações de uma entidade operando na estrutura SNMPv1, ela converte as interceptações no formato SNMPv2C. Portanto, quando o [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) entrega uma interceptação, ele está sempre no formato SNMPv2c. RFC 1908, "coexistência entre a versão 1 e a versão 2 da estrutura de gerenciamento de rede padrão da Internet", especifica as regras para a tradução do SNMPv1 para o formato de interceptação de SNMPv2C.

Um aplicativo WinSNMP pode verificar a última entrada de associação de variável em uma lista de associação de variável para determinar se a entrada é uma interceptação convertida de SNMPv1 para o formato SNMPv2C. Nesse caso, a última Associação de variável será sempre igual ao valor "snmpTrapEnterpriseOID. 0".

Para obter mais informações, consulte [Gerenciando interceptações e notificações](managing-traps-and-notifications.md).

 

 




