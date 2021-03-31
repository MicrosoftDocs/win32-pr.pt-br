---
title: Criando uma PDU
description: Para criar e inicializar uma PDU, um aplicativo WinSNMP chama a função SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822653"
---
# <a name="creating-a-pdu"></a>Criando uma PDU

Para criar e inicializar uma PDU, um aplicativo WinSNMP chama a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . O aplicativo deve chamar **SnmpCreatePdu** antes de chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que a implementação do Microsoft WINSNMP transmita uma PDU. O aplicativo também deve chamar [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) antes de chamar a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) para solicitar codificação de uma mensagem SNMP.

O aplicativo deve chamar a função [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) para liberar os recursos que a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aloca para uma nova PDUs.

 

 




