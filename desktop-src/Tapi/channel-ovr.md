---
description: Cada linha tem um ou mais canais. Os provedores de serviço normalmente tratam como os canais são expostos como endereços a um aplicativo, e o usuário final ou o servidor não requer conhecimento específico de canais.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502050"
---
# <a name="channel-telephony-api"></a>Canal (API de telefonia)

Cada linha tem um ou mais canais. Os provedores de serviço normalmente tratam como os canais são expostos como endereços a um aplicativo, e o usuário final ou o servidor não requer conhecimento específico de canais.

Os canais são idênticos e, portanto, intercambiáveis. Em POTS (serviço de telefone antigo), exatamente um canal existe em uma linha e o canal é usado exclusivamente para voz. Com o ISDN, pelo menos três (e até 30 ou mais) canais podem existir em uma linha simultaneamente.

Cada canal pode ter seu próprio endereço, o que significa que uma linha pode ter tantos endereços quantos tenham canais. A relação exata entre canais e endereços expostos a um aplicativo depende da implementação de um provedor de serviços.

Alguns provedores de serviços dão suporte à atribuição de mais de um endereço a um único canal. Em linhas POTS, vários endereços são possibilitados por vários sistemas, como DID (Direct Inward Dialing) ou toque distintivo, que são serviços de tarifa adicional que a empresa telefônica fornece.

Muitas grandes corporações usam o DID para chamadas de entrada. Antes de uma chamada ser conectada, seu número de extensão de destino é sinalizado para o PBX, o que faz com que a extensão toque em vez do telefone do operador. Um exemplo de toque distintivo em uma casa privada seria se os pais usavam um endereço, os filhos, outro e um computador de fax um terceiro. Como apenas uma linha conecta a casa à rede telefônica, todos os telefones tocam quando uma chamada é exibida, mas o padrão de anel é diferente dependendo do número que a parte de chamada tiver discado. Com o toque distintivo, as pessoas sabem a quem é a chamada de entrada e a máquina de fax responde suas chamadas reconhecendo seu próprio estilo de toque.

No ISDN, os vários canais B podem não ter endereços separados. Como esses B canais podem estar no mesmo endereço, é o provedor de serviços (e não o aplicativo ou uma pessoa que tenha discado o número) que atribui chamadas a esses canais.

 

 



