---
title: Resposta correspondente e PDUs de solicitação
description: A ordem na qual o aplicativo WinSNMP recebe respostas SNMP pode não corresponder à ordem em que o aplicativo envia solicitações de operação SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009314"
---
# <a name="matching-response-and-request-pdus"></a>Resposta correspondente e PDUs de solicitação

A ordem na qual o aplicativo WinSNMP recebe respostas SNMP pode não corresponder à ordem em que o aplicativo envia solicitações de operação SNMP. Para corresponder à resposta com a solicitação, o aplicativo deve usar o campo identificador de solicitação ( **a \_ ID da solicitação**) da resposta.

O **campo \_ ID da solicitação** é um valor numérico exclusivo que identifica a PDU. Os aplicativos podem atribuir identificadores de solicitação chamando a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Chame a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) para recuperar a ID de **solicitação \_** de uma PDU.

 

 




