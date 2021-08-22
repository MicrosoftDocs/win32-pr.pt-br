---
title: Nomes de host e endereços IP
description: As redes TCP/IP exigem que os nomes de host sejam resolvidos para endereços IP antes que as informações de endereço possam ser usadas para criar uma conexão.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Endereços IP e nomes de host SNMP
- Nomes de host, resolvendo SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f884f8ed681a5fc4864665f4c2a97ef8ed9fc0d81756d51848428b76163f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009504"
---
# <a name="host-names-and-ip-addresses"></a>Nomes de host e endereços IP

As redes TCP/IP exigem que os nomes de host sejam resolvidos para endereços IP antes que as informações de endereço possam ser usadas para criar uma conexão. os computadores em execução no sistema operacional Windows usam um arquivo de host que, para essa finalidade, mapeia nomes de host para endereços IP.

O arquivo de host é um arquivo de texto que lista nomes de host explícitos e endereços IP. O arquivo de host é carregado automaticamente na memória na inicialização e consultado quando um nome de host requer resolução. Se o arquivo de host não contiver as informações de mapeamento necessárias para resolver um nome de host específico para seu endereço IP, uma consulta de resolução será feita em um servidor DNS.

o SNMP usa o Windows Internet Serviço de Nomenclatura (WINS) para resolução de nome de host. O WINS torna possível mapear nomes NetBIOS ou nomes de computador para endereços IP em redes TCP/IP. Se o computador não puder acessar um servidor WINS, o serviço SNMP usará o arquivo de host para resolver nomes de host para endereços IP.

O serviço SNMP dá suporte ao uso de nomes de host e endereços IP. No entanto, quando você tem a opção de usar nomes de host ou endereços IP para identificar locais de rede, seus aplicativos de gerenciamento SNMP devem usar nomes de host. Se você usar nomes de host, adicione todos os mapeamentos de nome de host e endereço IP dos sistemas participantes ao arquivo de host.

 

 




