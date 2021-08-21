---
description: Cada linha tem um ou mais canais. Os provedores de serviços normalmente lidam com a forma como os canais são expostos como endereços para um aplicativo e o usuário final ou o servidor não exige conhecimento específico dos canais.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de Telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f15c6ede88635bdd93fe5a06955c91a0a13286731ff02310f0b690f9bd01445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869695"
---
# <a name="channel-telephony-api"></a>Canal (API de Telefonia)

Cada linha tem um ou mais canais. Os provedores de serviços normalmente lidam com a forma como os canais são expostos como endereços para um aplicativo e o usuário final ou o servidor não exige conhecimento específico dos canais.

Os canais são idênticos e, portanto, intercambiáveis. No POTS (Serviço de Telefone Simples Antigo), há exatamente um canal em uma linha e o canal é usado exclusivamente para voz. Com o ISDN, pelo menos três (e até 30 ou mais) canais podem existir em uma linha simultaneamente.

Cada canal pode ter seu próprio endereço, o que significa que uma linha pode ter tantos endereços quanto canais. A relação precisa entre canais e endereços expostos a um aplicativo depende da implementação de um provedor de serviços.

Alguns provedores de serviços suportam a atribuição de mais de um endereço a um único canal. Em linhas DOIS, vários endereços são possibilitados por vários sistemas, como DID (discagem direta interna) ou toque distinto, que são serviços de tarifa extra que a empresa de telefone fornece.

Muitas grandes empresas usam DID para chamadas de entrada. Antes que uma chamada seja conectada, seu número de extensão de destino é sinalizado para o PBX, o que faz com que a extensão toque em vez do telefone do operador. Um exemplo de toque distinto em uma casa privada seria se os pais usavam um endereço, os filhos outro e um computador de fax um terceiro. Como apenas uma linha conecta a casa à rede telefônica, todos os telefones tocarão quando uma chamada for exibida, mas o padrão de anel será diferente dependendo do número discado pela parte de chamada. Com um toque distinto, as pessoas sabem para quem é a chamada de entrada e o computador de fax responde às chamadas reconhecendo seu próprio estilo de toque.

No ISDN, os vários canais B podem não ter endereços separados. Como esses canais B podem estar no mesmo endereço, é o provedor de serviços (e não o aplicativo ou uma pessoa que discou o número) que atribui chamadas a esses canais.

 

 



