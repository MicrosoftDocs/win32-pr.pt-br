---
description: As nuvens são usadas pelas infraestruturas de Agrupamento de Pares e Grafo.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Nuvens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5ecbeee1f5b69d120c5f351f8a5bb200b6e3e5f60e4bacca5a4f5484f402dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932688"
---
# <a name="clouds"></a>Nuvens

As nuvens são usadas pelas infraestruturas [de Agrupamento](grouping-api.md) de Pares [e Grafo.](graphing-api.md) O [PROTOCOLO PNRP identifica](pnrp-namespace-provider-api.md) uma nuvem como um conjunto de pares que podem se comunicar dentro do mesmo escopo IPv6. As nuvens estão intimamente relacionadas aos escopos IPv6. A lista a seguir identifica alguns dos recursos de nuvem exclusivos:

-   Uma nuvem é identificada por um nome e as nuvens disponíveis podem ser enumeradas usando [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Se um computador estiver conectado à Internet, ele faz parte de uma nuvem global, que é identificada pela cadeia de caracteres \_ "Global".
-   Se um computador estiver conectado a uma ou mais redes locais (LAN), nuvens individuais estarão disponíveis para cada link.
-   Um computador pode ser conectado a várias redes tendo vários adaptadores de rede ou usando uma VPN (rede virtual privada), o que significa que um computador com uma interface pode ser visível em muitas nuvens.
-   Você pode usar o PNRP para registrar e resolver nomes de pares em uma nuvem específica.

 

 



