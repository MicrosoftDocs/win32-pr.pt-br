---
title: Alterando a política de retransmissão
description: A implementação do Microsoft WinSNMP fornece suporte à política de retransmissão ao armazenar um valor de tempo-out e uma contagem de novas tentativa para o aplicativo WinSNMP em um banco de dados.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed160de40b300d1b2430304b7a487f4544fee9a13db6049d1d837958276da8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009764"
---
# <a name="changing-the-retransmission-policy"></a>Alterando a política de retransmissão

A implementação do Microsoft WinSNMP fornece suporte à política de retransmissão ao armazenar um valor de tempo-out e uma contagem de novas tentativa para o aplicativo WinSNMP em um banco de dados. A implementação armazena valores para entidades de destino individuais. Inicialmente, a implementação fornece valores padrão para esses elementos, mas um aplicativo pode adicionar ou modificar valores para entidades individuais.

Uma chamada para as funções [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) e [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) retorna os valores de contagem de tempo-out e de nova tentativa para uma entidade de destino específica. Para alterar o valor de tempo-máximo, um aplicativo WinSNMP deve chamar a [**função SnmpSetTimeout.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) Para alterar o valor da contagem de novas tentar, o aplicativo deve chamar a [**função SnmpSetRetry.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) As configurações atualizadas afetam novas solicitações de mensagem SNMP para a entidade de destino.

 

 




