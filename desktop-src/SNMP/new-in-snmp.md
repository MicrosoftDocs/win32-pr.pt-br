---
title: Novidades no SNMP
description: O SNMP dá suporte ao uso de IPv6 a partir do Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641720"
---
# <a name="new-in-snmp"></a>Novidades no SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

O SNMP dá suporte ao uso de IPv6 a partir do Windows Vista. No entanto, o SNMP dá suporte a IPv6 somente para redes que executam o Windows Server 2008 e o Windows Vista. Isso ocorre porque o SNMP requer a pilha de protocolos atualizada disponível nesses sistemas operacionais para seu suporte IPv6.

A menos que sua rede seja exclusivamente uma rede do Windows Server 2008, as comunicações IPv6 falharão, mesmo que uma pilha de protocolo IPv6 seja instalada separadamente nesses computadores que executam versões anteriores do Windows. Por exemplo, agentes SNMP executados no Windows Server 2003, ou Windows XP ou Windows 2000, respondem somente a consultas feitas em seus endereços IPv4.

 

 