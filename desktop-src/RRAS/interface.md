---
title: Interface (RRAS)
description: Uma interface é uma conexão lógica com uma rede. Cada interface é identificada por um índice exclusivo. Os protocolos de roteamento multicast (como MOSPF) lidam com todos os tipos de interfaces da mesma forma.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917887"
---
# <a name="interface-rras"></a>Interface (RRAS)

Uma interface é uma conexão lógica com uma rede. Cada interface é identificada por um índice exclusivo. Os protocolos de roteamento multicast (como MOSPF) lidam com todos os tipos de interfaces da mesma forma.

No caso de uma interface de LAN, a interface corresponde a um dispositivo físico real no computador (o adaptador de LAN). No caso de uma interface WAN, a interface é mapeada para uma porta quando uma conexão é estabelecida. As interfaces WAN podem ser baseadas em túneis e a porta pode ser uma porta de rede virtual privada (VPN).

Os sistemas operacionais Windows 2000 e posteriores dão suporte a uma interface "ponto a multiponto". Esse tipo de interface pode ser exibido como uma coleção de links ponto a ponto que compartilham um único ponto de rescisão.

Para identificar exclusivamente um link exato em uma interface ponto a multiponto, a API MGM usa o endereço do próximo salto da ID da interface. Para dar suporte a essa identificação, a API MGM usa uma ID de interface estendida, que inclui um endereço de [próximo salto](next-hop.md) .

 

 




