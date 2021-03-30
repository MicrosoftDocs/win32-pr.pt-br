---
title: Atribuindo identificadores de solicitação
description: Um aplicativo WinSNMP pode chamar a função SnmpCreatePdu ou a função SnmpSetPduData para atribuir um identificador de solicitação gerado pelo aplicativo a um PDU. O aplicativo deve passar o valor no \_ parâmetro ID da solicitação.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634841"
---
# <a name="assigning-request-identifiers"></a>Atribuindo identificadores de solicitação

Um aplicativo WinSNMP pode chamar a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) para atribuir um identificador de solicitação gerado pelo aplicativo a um PDU. O aplicativo deve passar o valor no parâmetro *\_ ID da solicitação* .

Um aplicativo pode solicitar que a implementação do Microsoft WinSNMP gere e atribua um identificador de solicitação a um PDU passando zero no *parâmetro \_ ID da solicitação* da função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . O aplicativo pode recuperar o identificador de solicitação atribuído com uma chamada para a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .

Para atribuir um identificador de solicitação igual a um valor específico, incluindo zero, o aplicativo deve passar esse valor no *parâmetro \_ ID da solicitação* da função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

Quando a implementação executa a política de retransmissão do aplicativo, ela inclui o **campo \_ ID da solicitação** do PDU original em cada mensagem SNMP retransmitida. Para obter mais informações, consulte [sobre a retransmissão](about-retransmission.md) e [Gerenciamento da política de retransmissão](managing-the-retransmission-policy.md).

> [!Note]  
> Quando a implementação recebe interceptações de uma entidade SNMPv1, ela atribui um valor diferente de zero ao campo **\_ ID da solicitação** da PDU. Esse valor pode duplicar um identificador de solicitação usado pelo aplicativo em uma PDU de solicitação. Os aplicativos devem verificar a duplicação.

 

 

 




