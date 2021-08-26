---
description: Muitos aplicativos registram erros e eventos em logs de erros proprietários, cada um com seu próprio formato e interface do usuário.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Log de eventos (log de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8894c7a6d038efdc317611ca6284f62d99c82ebc767b6f96f83931803a887185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927836"
---
# <a name="event-logging-event-logging"></a>Log de eventos (log de eventos)

Muitos aplicativos registram erros e eventos em logs de erros proprietários, cada um com seu próprio formato e interface do usuário. Dados de diferentes aplicativos não podem ser mesclados facilmente em um relatório completo, exigindo que os administradores do sistema ou representantes de suporte verifiquem uma variedade de fontes para diagnosticar problemas.

O log de eventos fornece uma maneira padrão e centralizada para aplicativos (e o sistema operacional) para registrar eventos importantes de software e hardware. O serviço de log de eventos registra eventos de várias fontes e os armazena em uma única coleção chamada *log de eventos*. O Visualizador de Eventos permite que você exiba logs; a interface de programação também permite que você examine os logs.

-   [Sobre o log de eventos](about-event-logging.md)
-   [Usando o log de eventos](using-event-logging.md)
-   [Referência de log de eventos](event-logging-reference.md)

> [!Note]  
> a API de log de eventos foi desenvolvida para aplicativos executados no sistema operacional Windows Server 2003, Windows XP ou Windows 2000. no Windows Vista, a infraestrutura de log de eventos foi reprojetada. os aplicativos projetados para execução em Windows Vista ou sistemas operacionais posteriores devem usar [Windows log de eventos](/windows/desktop/WES/windows-event-log) para registrar eventos.
