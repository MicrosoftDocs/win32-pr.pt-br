---
title: Quais são as ações básicas da API do ponto de controle
description: Todos os pontos de controle executam as tarefas a seguir.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a102c389a41b32fd7a79bf749ce38f1267912c3993e2461adac9b6730ea92325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513636"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Quais são as Ações Básicas da API do Ponto de Controle?

Todos os pontos de controle executam as seguintes tarefas:

-   Encontre dispositivos baseados em UPnP disponíveis na rede.
-   Determine quais desses dispositivos são de interesse.
-   Emitir solicitações de controle para os dispositivos de interesse e receber eventos gerados pelos dispositivos.

Um aplicativo deve primeiro encontrar dispositivos baseados em UPnP disponíveis na rede executando uma pesquisa. Como os critérios de pesquisa definidos pela arquitetura UPnP são bastante amplos, o aplicativo pode encontrar mais dispositivos do que são necessários. Portanto, o aplicativo deve examinar as características dos dispositivos encontrados para determinar quais deles mais se aproximam dos critérios de pesquisa. O aplicativo pode emitir solicitações de controle para esses dispositivos.

As seções a seguir descrevem como executar essas operações usando a API do Ponto de Controle com a tecnologia UPnP:

-   [Localizar dispositivos](finding-devices.md)
-   [Descrevendo dispositivos](describing-devices.md)
-   [Controlando dispositivos](controlling-devices.md)

Para ver a documentação detalhada sobre cada interface na API do Ponto de Controle, consulte [Referência da API do Ponto de Controle](control-point-api-with-upnp-technology-reference.md).

 

 




