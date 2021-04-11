---
description: A TAPI 2,0 fornece um pequeno número de aprimoramentos para a funcionalidade básica da TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296734"
---
# <a name="tapi-20"></a>TAPI 2,0

A TAPI 2,0 fornece um pequeno número de aprimoramentos para a funcionalidade básica da TAPI 1,4. No entanto, houve algumas grandes alterações arquitetônicas que melhoraram muito sua estabilidade. A maioria das alterações foram as alterações fundamentais necessárias para colocar a TAPI no Windows NT 4,0 e aproveitar seus recursos (suporte completo a 32 bits, serviços e Unicode). No entanto, essas alterações eram internas à TAPI e tinham pouco efeito em aplicativos TAPI.

Os aplicativos que dão suporte a TAPI 1,3 e 1,4 (aplicativos de 16 bits por meio de uma camada de conversão) funcionam bem em sistemas operacionais Windows Server 2003, Windows XP, Windows 2000 e Windows NT. No entanto, o efeito nos desenvolvedores do provedor de serviços era significativo. Os provedores de serviço para esses sistemas operacionais devem ser DLLs Unicode de 32 bits que podem ser executadas no contexto de TAPISRV, não no contexto do aplicativo TAPI (como fazia todas as TSPs anteriores baseadas em Win16). O TSPs desenvolvido para TAPI 1,4 não funciona em sistemas operacionais Windows Server 2003, Windows XP, Windows 2000 ou Windows NT.

A TAPI 2,0 também adiciona os recursos importantes do suporte ao Call Center e ao suporte de QOS (qualidade de serviço).

Os binários do sistema TAPI fornecidos com o Windows oferecem suporte a TAPI versões 1,3 e 1,4 para todos os aplicativos. No entanto, os aplicativos de 16 bits não podem usar a TAPI 2,0 e não é possível usar um TSP 2. x de TAPI de 16 bits.

 

 



