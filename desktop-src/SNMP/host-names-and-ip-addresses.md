---
title: Nomes de host e endereços IP
description: As redes TCP/IP exigem que os nomes de host sejam resolvidos para endereços IP antes que as informações de endereço possam ser usadas para criar uma conexão.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Endereços IP e nomes de host SNMP
- Nomes de host, resolvendo SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635595"
---
# <a name="host-names-and-ip-addresses"></a>Nomes de host e endereços IP

As redes TCP/IP exigem que os nomes de host sejam resolvidos para endereços IP antes que as informações de endereço possam ser usadas para criar uma conexão. Os computadores em execução no sistema operacional Windows usam um arquivo de host que, para essa finalidade, mapeia nomes de host para endereços IP.

O arquivo de host é um arquivo de texto que lista nomes de host explícitos e endereços IP. O arquivo de host é carregado automaticamente na memória na inicialização e consultado quando um nome de host requer resolução. Se o arquivo de host não contiver as informações de mapeamento necessárias para resolver um nome de host específico para seu endereço IP, uma consulta de resolução será feita em um servidor DNS.

O SNMP usa o WINS (Windows Internet Serviço de Nomenclatura) para resolução de nomes de host. O WINS torna possível mapear nomes NetBIOS ou nomes de computador para endereços IP em redes TCP/IP. Se o computador não puder acessar um servidor WINS, o serviço SNMP usará o arquivo de host para resolver nomes de host para endereços IP.

O serviço SNMP dá suporte ao uso de nomes de host e endereços IP. No entanto, quando você tem a opção de usar nomes de host ou endereços IP para identificar locais de rede, seus aplicativos de gerenciamento SNMP devem usar nomes de host. Se você usar nomes de host, adicione todos os mapeamentos de nome de host e endereço IP dos sistemas participantes ao arquivo de host.

 

 




