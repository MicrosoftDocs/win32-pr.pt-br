---
description: Uma difusão geral pela Internet é feita definindo os campos sa netnum e sa nodenum como \_ \_ binários (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Difusão de todas as rotas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a5f0ba1e900dd390610a3bd3af2f779d523ae4a08973596e7da6b8331acc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322713"
---
# <a name="all-routes-broadcast"></a>Difusão de todas as rotas

Uma difusão geral pela Internet é feita definindo os campos **sa \_ netnum** e **sa \_ nodenum** como binários (1). O provedor de serviços converte essa solicitação em um pacote de tipo 20, que os roteadores IPX reconhecem e encaminham. O pacote visita todas as sub-redes e pode ser duplicado várias vezes. Os receptores devem manipular várias cópias duplicadas do datagrama.

O uso desse tipo de difusão não é popular entre os administradores de rede, portanto, seu uso deve ser extremamente limitado. Muitos roteadores desabilitam esse tipo de difusão, deixando partes da sub-rede invisíveis para o pacote.

 

 



