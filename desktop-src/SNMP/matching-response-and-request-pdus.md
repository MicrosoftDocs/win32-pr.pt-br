---
title: Resposta correspondente e PDUs de solicitação
description: A ordem na qual o aplicativo WinSNMP recebe respostas SNMP pode não corresponder à ordem em que o aplicativo envia solicitações de operação SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916449"
---
# <a name="matching-response-and-request-pdus"></a>Resposta correspondente e PDUs de solicitação

A ordem na qual o aplicativo WinSNMP recebe respostas SNMP pode não corresponder à ordem em que o aplicativo envia solicitações de operação SNMP. Para corresponder à resposta com a solicitação, o aplicativo deve usar o campo identificador de solicitação ( **a \_ ID da solicitação**) da resposta.

O **campo \_ ID da solicitação** é um valor numérico exclusivo que identifica a PDU. Os aplicativos podem atribuir identificadores de solicitação chamando a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Chame a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) para recuperar a ID de **solicitação \_** de uma PDU.

 

 




