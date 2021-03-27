---
description: As sessões de rastreamento de eventos registram eventos de um ou mais provedores habilitados por um controlador.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sessões de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce49453881d9106119dab15b64ac0698e9a493f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829044"
---
# <a name="event-tracing-sessions"></a>Sessões de rastreamento de eventos

As sessões de rastreamento de eventos registram eventos de um ou mais [provedores](providing-events.md) habilitados por um [controlador](controlling-event-tracing-sessions.md) . A sessão também é responsável por gerenciar e liberar os buffers. O controlador define a sessão, que normalmente inclui a especificação do nome do arquivo de log e da sessão, tipo de arquivo de log a ser usado e a resolução do carimbo de data/hora usado para registrar os eventos.

O rastreamento de eventos dá suporte a um máximo de 64 sessões de rastreamento de eventos em execução simultaneamente. Dessas sessões, há duas sessões de finalidade especial. As sessões restantes estão disponíveis para uso geral. As duas sessões de finalidade especial são:

-   Sessão global de agente
-   Sessão do NT kernel logger

A sessão de rastreamento de eventos do agente global registra eventos que ocorrem no início do processo de inicialização do sistema operacional, como aqueles gerados por drivers de dispositivo. Para obter informações sobre como configurar a sessão de rastreamento de eventos do agente global, consulte [Configurando e iniciando a sessão global do agente](configuring-and-starting-the-global-logger-session.md).

A sessão de rastreamento de evento NT kernel logger registra eventos de sistema predefinidos gerados pelo sistema operacional, por exemplo, e/s de disco ou eventos de falha de página. Para obter informações sobre como configurar a sessão de rastreamento de eventos NT kernel Logger, [Configurando e iniciando a sessão do agente de log do NT kernel](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obter informações sobre como definir uma sessão de rastreamento de eventos regular, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Dá suporte apenas a sessões de rastreamento de eventos 32.

 

 



