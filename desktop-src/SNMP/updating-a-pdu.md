---
title: Atualizando uma PDU
description: Um aplicativo WinSNMP pode recuperar e atualizar campos de PDU selecionados usando as funções SnmpGetPduData e SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636847"
---
# <a name="updating-a-pdu"></a>Atualizando uma PDU

Um aplicativo WinSNMP pode recuperar e atualizar campos de PDU selecionados usando as funções [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) e [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

O aplicativo pode recuperar o tipo de PDU, o identificador de solicitação, o status de erro e os campos de índice de erro de um PDU específico. Ele também pode recuperar o identificador para a lista de associação de variáveis. O aplicativo pode atualizar o **\_ tipo de PDU** e os campos de **\_ ID de solicitação** .

Se o tipo de PDU for igual ao SNMP \_ PDU \_ em massa, o aplicativo também poderá atualizar os campos de **não \_ repetições** e as **\_ repetições máximas** da PDU.

 

 




