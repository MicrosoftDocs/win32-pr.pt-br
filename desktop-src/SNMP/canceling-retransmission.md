---
title: Cancelando a retransmissão
description: Se não houver resposta a uma solicitação de comunicação dentro do período de tempo limite especificado para uma entidade de destino e se as retransmissões forem especificadas para a entidade, a implementação do Microsoft WinSNMP retransmitirá a solicitação.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005512"
---
# <a name="canceling-retransmission"></a>Cancelando a retransmissão

Se não houver resposta a uma solicitação de comunicação dentro do período de tempo limite especificado para uma entidade de destino e se as retransmissões forem especificadas para a entidade, a implementação do Microsoft WinSNMP retransmitirá a solicitação. Uma chamada para a função [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) pode cancelar esse ciclo de retransmissão e liberar estruturas de dados internas associadas à solicitação de mensagem.

Observe que é possível que uma entidade de destino receba uma mensagem SNMP que foi cancelada por uma chamada para a função [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) . Também é possível que uma entidade de destino possa responder a uma mensagem SNMP cancelada. Isso acontece porque o serviço de enfileiramento de transações ocorre em vários níveis. No entanto, depois que uma mensagem for cancelada por uma chamada para [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), a implementação do Microsoft WinSNMP não retransmitirá a mensagem, enviará uma PDU de resposta ou enviará uma notificação de tempo limite para o aplicativo para essa mensagem.

 

 




