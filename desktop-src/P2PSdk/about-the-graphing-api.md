---
description: A API de grafo de pares permite que os aplicativos transmitam dados entre os colegas de forma eficiente e confiável. Os principais conceitos da tecnologia de grafo de pares são os nós de um grafo de mesmo nível e avisos de eventos.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Sobre a API de gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735bf7993744aa8d1e76b8c5d98e8d6856bb4e1757224cd0c98f2e7b1b6f710b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011784"
---
# <a name="about-the-graphing-api"></a>Sobre a API de gráfico

A API de grafo de pares permite que os aplicativos transmitam dados entre os colegas de forma eficiente e confiável. Os principais conceitos da tecnologia de grafo de pares são os **nós** de um grafo de mesmo nível e avisos de eventos.

## <a name="nodes"></a>Nós

Um nó representa uma instância específica de um par em uma rede. A infraestrutura de API de grafo de pares garante que cada nó tenha uma exibição consistente dos dados em um grafo. Um nó tem os seguintes recursos:

-   Pode se conectar a um nó diferente e formar uma rede interrelacionada chamada de grafo par.
-   Pode compartilhar dados com outros nós em um grafo na forma de um [registro](records.md).
-   Pode criar conexões diretas separadas dos gráficos pares estabelecidos usando a [API de agrupamento](about-the-grouping-api.md)de pares.
    > [!Note]  
    > Conexões diretas permitem que os nós enviem dados privados entre si.

     

## <a name="event-notices"></a>Avisos de eventos

A API de grafo de pares tem uma infraestrutura de eventos que permite que um aplicativo se registre e receba um aviso de um evento de mesmo nível dentro da infraestrutura da API de grafo de pares. Quando algo é alterado em um grafo de mesmo nível, um aplicativo envia um aviso de evento para identificar que ocorreu uma alteração.

 

 



