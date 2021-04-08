---
title: Alterando a política de retransmissão
description: A implementação do Microsoft WinSNMP fornece suporte à política de retransmissão, armazenando um valor de tempo limite e uma contagem de repetição para o aplicativo WinSNMP em um banco de dados.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822654"
---
# <a name="changing-the-retransmission-policy"></a>Alterando a política de retransmissão

A implementação do Microsoft WinSNMP fornece suporte à política de retransmissão, armazenando um valor de tempo limite e uma contagem de repetição para o aplicativo WinSNMP em um banco de dados. A implementação armazena valores para entidades de destino individuais. A implementação inicialmente fornece valores padrão para esses elementos, mas um aplicativo pode adicionar ou modificar valores para entidades individuais.

Uma chamada para as funções [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) e [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) retorna os valores de tempo limite e de contagem de repetição para uma entidade de destino específica. Para alterar o valor de tempo limite, um aplicativo WinSNMP deve chamar a função [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) . Para alterar o valor de contagem de repetição, o aplicativo deve chamar a função [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) . As configurações atualizadas afetam as novas solicitações de mensagens SNMP para a entidade de destino.

 

 




