---
description: As sessões de rastreamento de eventos registram eventos de um ou mais provedores habilitados por um controlador.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sessões de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2edfe4bdfaf621575d8f2f8ab7d81a09aae8bfbddcb3f63890c4083378bb905b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083236"
---
# <a name="event-tracing-sessions"></a>Sessões de rastreamento de eventos

As sessões de rastreamento de eventos registram eventos de um ou [mais provedores](providing-events.md) habilitados [por um](controlling-event-tracing-sessions.md) controlador. A sessão também é responsável por gerenciar e liberar os buffers. O controlador define a sessão, que normalmente inclui especificar a sessão e o nome do arquivo de log, o tipo de arquivo de log a ser usado e a resolução do carimbo de data/hora usado para registrar os eventos.

O Rastreamento de Eventos dá suporte a um máximo de 64 sessões de rastreamento de eventos em execução simultaneamente. Dessas sessões, há duas sessões de finalidade especial. As sessões restantes estão disponíveis para uso geral. As duas sessões de finalidade especial são:

-   Sessão do Global Logger
-   Sessão do NT Kernel Logger

A sessão de rastreamento de eventos do Global Logger registra eventos que ocorrem no início do processo de inicialização do sistema operacional, como aqueles gerados por drivers de dispositivo. Para obter informações sobre como configurar a sessão de rastreamento de eventos do Global Logger, consulte [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).

A sessão de rastreamento de eventos do NT Kernel Logger registra eventos predefinidos do sistema gerados pelo sistema operacional, por exemplo, eventos de falha de página ou E/S de disco. Para obter informações sobre como configurar a sessão de rastreamento de eventos do NT Kernel Logger, Configurando e iniciando a sessão do [NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obter informações sobre como definir uma sessão regular de rastreamento de eventos, consulte Configurando e [iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Dá suporte a apenas 32 sessões de rastreamento de eventos.

 

 



