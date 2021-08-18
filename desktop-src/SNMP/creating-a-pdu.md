---
title: Criando uma PDU
description: Para criar e inicializar uma PDU, um aplicativo WinSNMP chama a função SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009594"
---
# <a name="creating-a-pdu"></a>Criando uma PDU

Para criar e inicializar uma PDU, um aplicativo WinSNMP chama a [**função SnmpCreatePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) O aplicativo deve chamar **SnmpCreatePdu** antes de chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que a implementação do Microsoft WinSNMP transmita uma PDU. O aplicativo também deve chamar [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) antes de chamar a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) para solicitar a codificação de uma mensagem SNMP.

O aplicativo deve chamar a [**função SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) para liberar os recursos que a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aloca para novas PDUs.

 

 




