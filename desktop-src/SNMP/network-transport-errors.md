---
title: Erros de transporte de rede
description: A implementação do Microsoft WinSNMP pode detectar um erro de transporte de rede depois de transmitir uma mensagem SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823924"
---
# <a name="network-transport-errors"></a>Erros de transporte de rede

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

A implementação do Microsoft WinSNMP pode detectar um erro de transporte de rede depois de transmitir uma mensagem SNMP. Quando isso ocorre, a implementação envia uma notificação de recebimento de dados para a sessão WinSNMP que iniciou a solicitação de comunicação. A implementação também retorna falha de SNMPAPI \_ na próxima chamada para a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para a sessão. A função **SnmpRecvMsg** falha com um código de erro estendido que indica um erro de camada de transporte de rede.

Para obter uma lista de erros de camada de transporte específicos, consulte as páginas de referência para as funções [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)e [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 