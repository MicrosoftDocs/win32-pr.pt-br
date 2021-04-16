---
description: Muitos aplicativos registram erros e eventos em logs de erros proprietários, cada um com seu próprio formato e interface do usuário.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Log de eventos (log de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779222"
---
# <a name="event-logging-event-logging"></a>Log de eventos (log de eventos)

Muitos aplicativos registram erros e eventos em logs de erros proprietários, cada um com seu próprio formato e interface do usuário. Dados de diferentes aplicativos não podem ser mesclados facilmente em um relatório completo, exigindo que os administradores do sistema ou representantes de suporte verifiquem uma variedade de fontes para diagnosticar problemas.

O log de eventos fornece uma maneira padrão e centralizada para aplicativos (e o sistema operacional) para registrar eventos importantes de software e hardware. O serviço de log de eventos registra eventos de várias fontes e os armazena em uma única coleção chamada *log de eventos*. O Visualizador de Eventos permite que você exiba logs; a interface de programação também permite que você examine os logs.

-   [Sobre o log de eventos](about-event-logging.md)
-   [Usando o log de eventos](using-event-logging.md)
-   [Referência de log de eventos](event-logging-reference.md)

> [!Note]  
> A API de log de eventos foi projetada para aplicativos executados no sistema operacional Windows Server 2003, Windows XP ou Windows 2000. No Windows Vista, a infraestrutura de log de eventos foi reprojetada. Os aplicativos projetados para execução no Windows Vista ou em sistemas operacionais posteriores devem usar o [log de eventos do Windows](/windows/desktop/WES/windows-event-log) para registrar eventos.
