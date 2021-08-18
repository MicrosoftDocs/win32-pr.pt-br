---
description: Visão geral da notificação de eventos
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Visão geral da notificação de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ca5e6ffb4737054f773fc5be35d56939e711442a3b31761cd23c144ed00ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148529"
---
# <a name="overview-of-event-notification"></a>Visão geral da notificação de eventos

um filtro notifica o gerenciador de Graph de filtro sobre um evento postando uma notificação de evento. O evento pode ser algo esperado, como o fim de um fluxo, ou pode representar um erro, como uma falha para renderizar um fluxo. o filtro Graph Manager trata alguns eventos de filtro por si só, e deixa outros para que o aplicativo manipule. se o filtro Graph Manager não tratar um evento de filtro, ele colocará a notificação de eventos em uma fila. O grafo de filtro também pode enfileirar suas próprias notificações de eventos para o aplicativo.

Um aplicativo recupera eventos da fila e responde a eles com base no tipo de evento. a notificação de eventos em DirectShow, portanto, é semelhante ao esquema de enfileiramento de mensagens da Microsoft Windows. um aplicativo também pode cancelar o filtro Graph comportamento padrão do gerenciador para um determinado tipo de evento. o filtro Graph Manager, em seguida, coloca esses eventos diretamente na fila para que o aplicativo manipule.

Esse mecanismo habilita

-   o filtro Graph Manager para se comunicar com o aplicativo.
-   filtros para se comunicarem com o aplicativo e o filtro Graph Manager.
-   O aplicativo para determinar seu grau de envolvimento na manipulação de eventos.

 

 



