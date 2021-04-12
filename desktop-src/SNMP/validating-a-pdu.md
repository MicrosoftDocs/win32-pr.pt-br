---
title: Validando uma PDU
description: Quando o aplicativo WinSNMP chama a função SnmpSendMsg ou a função SnmpEncodeMsg, a implementação do Microsoft WinSNMP verifica a validade da PDU e os outros parâmetros de função.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364278"
---
# <a name="validating-a-pdu"></a>Validando uma PDU

Quando o aplicativo WinSNMP chama a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , a implementação do Microsoft WinSNMP verifica a validade da PDU e os outros parâmetros de função.

O valor de um componente de dados PDU (ou campo) pode ser válido individualmente, mas pode ser inválido em combinação com valores para outros campos. Por exemplo, a menos que o campo de **\_ tipo de PDU** da PDU seja uma resposta de PDU do SNMP \_ PDU \_ GetBulk ou SNMP \_ , os \_ campos **\_ status de erro** e **\_ índice de erro** devem ser iguais a zero. Qualquer outra combinação de valor constitui um PDU inválido.

A implementação rejeita PDUs inválidas e retorna o status de erro SNMPAPI \_ falha. Ele define um código de erro estendido igual a SNMPAPI \_ PDU \_ inválido.

 

 




