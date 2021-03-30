---
title: Quais são as ações básicas da API do ponto de controle
description: Todos os pontos de controle executam as seguintes tarefas.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e2db09aa8283034da20dc1bd2dc877bf0e5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636911"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Quais são as ações básicas da API do ponto de controle?

Todos os pontos de controle executam as seguintes tarefas:

-   Encontre dispositivos baseados em UPnP disponíveis na rede.
-   Determine quais desses dispositivos são interessantes.
-   Emitir solicitações de controle para os dispositivos de interesse e receber eventos gerados pelos dispositivos.

Um aplicativo deve primeiro localizar dispositivos baseados em UPnP disponíveis na rede executando uma pesquisa. Como os critérios de pesquisa definidos pela arquitetura de UPnP são bastante amplos, o aplicativo pode encontrar mais dispositivos do que o necessário. Portanto, o aplicativo deve examinar as características dos dispositivos que foram encontrados para determinar quais são mais semelhantes aos critérios de pesquisa. O aplicativo pode emitir solicitações de controle para esses dispositivos.

As seções a seguir descrevem como realizar essas operações usando a API do ponto de controle com tecnologia UPnP:

-   [Localizando dispositivos](finding-devices.md)
-   [Descrevendo dispositivos](describing-devices.md)
-   [Controlando dispositivos](controlling-devices.md)

Para obter uma documentação detalhada sobre cada interface na API do ponto de controle, consulte [referência da API do ponto de controle](control-point-api-with-upnp-technology-reference.md).

 

 




