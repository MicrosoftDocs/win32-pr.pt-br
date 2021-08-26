---
title: Interface (RRAS)
description: Uma interface é uma conexão lógica com uma rede. Cada interface é identificada por um índice exclusivo. Protocolos de roteamento multicast (como MOSPF) lidam com todos os tipos de interfaces da mesma forma.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1347f1a8d9afd049dd8283e7199c6da7d8a9dce6990a1e7ea674943f32811f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030156"
---
# <a name="interface-rras"></a>Interface (RRAS)

Uma interface é uma conexão lógica com uma rede. Cada interface é identificada por um índice exclusivo. Protocolos de roteamento multicast (como MOSPF) lidam com todos os tipos de interfaces da mesma forma.

No caso de uma interface LAN, a interface corresponde a um dispositivo físico real no computador (o adaptador de LAN). No caso de uma interface WAN, a interface é mapeada para uma porta quando uma conexão é estabelecida. As interfaces wan podem ser baseadas em túneis e a porta pode ser uma porta VPN (rede virtual privada).

Windows sistemas operacionais 2000 e posteriores são suportados por uma interface "ponto a ponto". Esse tipo de interface pode ser exibido como uma coleção de links ponto a ponto que compartilham um único ponto de término.

Para identificar exclusivamente um link exato em uma interface ponto a multiponto, a API do MGM usa o endereço do próximo salto da ID da interface. Para dar suporte a essa identificação, a API do MGM usa uma ID de interface estendida, que inclui um [endereço do próximo](next-hop.md) salto.

 

 




