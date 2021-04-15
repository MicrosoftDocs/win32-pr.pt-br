---
title: Associação ao ponto de início da pesquisa
description: O ponto de partida para uma pesquisa é um contêiner que contém diretamente ou indiretamente os objetos pesquisados.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, associação a um ponto de partida de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453477"
---
# <a name="binding-to-the-search-start-point"></a>Associação ao ponto de início da pesquisa

O ponto de partida para uma pesquisa é um contêiner que contém diretamente ou indiretamente os objetos pesquisados. A pesquisa não será executada em contêineres acima do ponto de início da pesquisa. Por exemplo, considere a seguinte estrutura de diretório hipotética:

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

Se uma pesquisa for executada para todos os objetos e o ponto de partida de pesquisa for "contêiner 2", somente o "objeto 3" e o "objeto 4" serão recuperados. Se a mesma pesquisa foi executada com o ponto de início de pesquisa em "contêiner 1", "objeto 1" e "objeto 2" seriam recuperados.

Para associar ao ponto de início da pesquisa, associe ao ADsPath do contêiner que será o ponto de partida de pesquisa.

 

 




