---
description: Visão geral da notificação de eventos
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Visão geral da notificação de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645916"
---
# <a name="overview-of-event-notification"></a>Visão geral da notificação de eventos

Um filtro notifica o Gerenciador de gráfico de filtro sobre um evento postando uma notificação de evento. O evento pode ser algo esperado, como o fim de um fluxo, ou pode representar um erro, como uma falha para renderizar um fluxo. O Gerenciador de gráficos de filtro trata alguns eventos de filtro por si só e deixa outros para que o aplicativo manipule. Se o Gerenciador do grafo de filtro não manipular um evento de filtro, ele colocará a notificação de eventos em uma fila. O grafo de filtro também pode enfileirar suas próprias notificações de eventos para o aplicativo.

Um aplicativo recupera eventos da fila e responde a eles com base no tipo de evento. A notificação de eventos no DirectShow é, portanto, semelhante ao esquema de enfileiramento de mensagens do Microsoft Windows. Um aplicativo também pode cancelar o comportamento padrão do Gerenciador de grafo de filtro para um determinado tipo de evento. O Gerenciador de gráfico de filtro coloca esses eventos diretamente na fila para que o aplicativo manipule.

Esse mecanismo habilita

-   O Gerenciador do grafo de filtro para se comunicar com o aplicativo.
-   Filtros para se comunicar com o aplicativo e o Gerenciador de gráfico de filtro.
-   O aplicativo para determinar seu grau de envolvimento na manipulação de eventos.

 

 



