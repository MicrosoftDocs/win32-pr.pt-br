---
description: As nuvens são usadas pelas infraestruturas de agrupamento e Grafação de pares.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Nuvens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091644"
---
# <a name="clouds"></a>Nuvens

As nuvens são usadas pelas infraestruturas de [agrupamento](grouping-api.md) e [grafação](graphing-api.md) de pares. O [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) identifica uma nuvem como um conjunto de pares que podem se comunicar dentro do mesmo escopo do IPv6. As nuvens estão fortemente relacionadas aos escopos de IPv6. A lista a seguir identifica alguns dos recursos de nuvem exclusivos:

-   Uma nuvem é identificada por um nome e as nuvens disponíveis podem ser enumeradas usando [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Se um computador estiver conectado à Internet, ele faz parte de uma nuvem global, que é identificada pela cadeia de caracteres "global \_ ".
-   Se um computador estiver conectado a uma ou mais redes locais (LAN), nuvens individuais estarão disponíveis para cada link.
-   Um computador pode ser conectado a várias redes por meio de vários adaptadores de rede ou usando uma VPN (rede virtual privada), o que significa que um computador com uma interface pode ser visível em muitas nuvens.
-   Você pode usar o PNRP para registrar e resolver nomes de pares em uma nuvem específica.

 

 



