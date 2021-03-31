---
title: Abrindo e fechando um aplicativo WinSNMP
description: O aplicativo WinSNMP deve chamar a função SnmpStartup com êxito antes de chamar qualquer outra função WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005844"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Abrindo e fechando um aplicativo WinSNMP

O aplicativo WinSNMP deve chamar a função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) com êxito antes de chamar qualquer outra função WinSNMP. A função **SnmpStartup** permite que a implementação do Microsoft WinSNMP execute procedimentos de inicialização. A função também retorna ao aplicativo a versão da API WinSNMP à qual a implementação dá suporte, o nível de comunicações SNMP que ele suporta e os modos de conversão e retransmissão padrão da implementação.

O aplicativo WinSNMP deve chamar a função [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) quando o aplicativo não exigir mais os serviços da implementação. Embora o **SnmpCleanup** permita que a implementação desaloque todos os recursos alocados para o aplicativo, é recomendável que o aplicativo chame primeiro a função [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) uma vez para cada sessão WinSNMP aberta, a fim de maximizar o desempenho da implementação. O aplicativo WinSNMP deve chamar [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) como a última função WinSNMP antes de ser encerrado.

 

 




