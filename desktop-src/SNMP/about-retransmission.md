---
title: Sobre a retransmissão
description: Um aplicativo WinSNMP pode fazer solicitações de operação SNMP de várias maneiras.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade0b2d58f371de87be5da855f26686a18518454c787c6a09e9701afbb731757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009954"
---
# <a name="about-retransmission"></a>Sobre a retransmissão

Um aplicativo WinSNMP pode fazer solicitações de operação SNMP de várias maneiras. O aplicativo pode emitir várias solicitações para um agente SNMP, sem aguardar uma resposta, ou pode emitir uma única solicitação e aguardar a resposta. Como o SNMP pode ser implementado em vários protocolos de transporte, os mecanismos de entrega e as características de confiabilidade podem variar.

Ao codificar o aplicativo WinSNMP, você deve determinar o nível de confiabilidade de que precisa para operações de comunicação, com base na maneira como o aplicativo emite solicitações de operação. Em seguida, você deve selecionar uma estratégia de retransmissão e implementar uma política de retransmissão.

Uma política de retransmissão inclui um período de tempo limite e uma contagem de repetição. Um período de tempo limite é o tempo decorrido, em centésimos de segundo, entre a emissão de um aplicativo de uma solicitação [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e seu recebimento da mensagem correspondente. O aplicativo recebe a mensagem como resultado de uma chamada para a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) . O valor de tempo limite é o período de tempo durante o qual a implementação do Microsoft WinSNMP aguarda uma entidade responder a uma solicitação de comunicação. Se não houver resposta dentro do período de tempo limite, a implementação retransmitirá a solicitação se o valor de contagem de repetição especificar tentativas de retransmissão ou falhar na chamada para [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg). Uma contagem de repetição é o número máximo de tentativas de retransmissão que a implementação faz se uma solicitação de transmissão SNMP falhar.

A implementação armazena valores de tempo limite e contagens de repetição em seu banco de dados para o aplicativo. A implementação armazena valores individuais para cada entidade de destino.

Os aplicativos devem estabelecer suas próprias frequências de sondagem e devem gerenciar variáveis de temporizador. Para obter mais informações, consulte [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md).

 

 




