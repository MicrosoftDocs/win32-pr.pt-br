---
title: Cancelando a retransmissão
description: Se não houver resposta a uma solicitação de comunicação dentro do período de tempo limite especificado para uma entidade de destino e se as retransmissões são especificadas para a entidade, a implementação do Microsoft WinSNMP retransmite a solicitação.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80770fc741357255adaa8b6bd15ab0e03b9148c37abf5fc631155d74b6d1f3a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009745"
---
# <a name="canceling-retransmission"></a>Cancelando a retransmissão

Se não houver resposta a uma solicitação de comunicação dentro do período de tempo limite especificado para uma entidade de destino e se as retransmissões são especificadas para a entidade, a implementação do Microsoft WinSNMP retransmite a solicitação. Uma chamada para a [**função SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) pode cancelar esse ciclo de retransmissão e liberar estruturas de dados internas associadas à solicitação de mensagem.

Observe que é possível que uma entidade de destino receba uma mensagem SNMP que foi cancelada por uma chamada para a [**função SnmpCancelMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) Também é possível que uma entidade de destino possa responder a uma mensagem SNMP cancelada. Isso ocorre porque a en fila de transações ocorre em vários níveis. No entanto, depois que uma mensagem tiver sido cancelada por uma chamada para [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), a implementação do Microsoft WinSNMP não retransmite a mensagem, envia uma PDU de resposta ou envia uma notificação de tempo limite para o aplicativo para essa mensagem.

 

 




