---
description: Quando ocorre um erro, o administrador do sistema ou o representante de suporte deve determinar o que causou o erro, tentar recuperar os dados perdidos e impedir que o erro seja recorrente.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Sobre o log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010603"
---
# <a name="about-event-logging"></a>Sobre o log de eventos

Quando ocorre um erro, o administrador do sistema ou o representante de suporte deve determinar o que causou o erro, tentar recuperar os dados perdidos e impedir que o erro seja recorrente. É útil se os aplicativos, o sistema operacional e outros serviços do sistema registram eventos importantes, como condições de pouca memória ou tentativas excessivas de acessar um disco. O administrador do sistema pode, então, usar o log de eventos para ajudar a determinar quais condições provocaram o erro e identificar o contexto no qual ele ocorreu. Ao Visualizar periodicamente o log de eventos, o administrador do sistema poderá identificar problemas (como um disco rígido com falha) antes que eles causem danos.

> [!Note]  
> A API de log de eventos foi projetada para aplicativos executados no sistema operacional Windows Server 2003, Windows XP ou Windows 2000. No Windows Vista, a infraestrutura de log de eventos foi reprojetada. Os aplicativos projetados para execução no Windows Vista ou em sistemas operacionais posteriores agora devem usar o [log de eventos do Windows](/windows/desktop/WES/windows-event-log) para registrar eventos.

 
Esta seção aborda a interface de programação para escrever e consumir eventos usando o log de eventos.

-   [Tipos de evento](event-types.md)
-   [Diretrizes de registro em log](logging-guidelines.md)
-   [Elementos de log de eventos](event-logging-elements.md)
-   [Operações de log de eventos](event-logging-operations.md)
-   [Modelo de log de eventos](event-logging-model.md)
-   [Segurança do log de eventos](event-logging-security.md)

> [!Note]  
> Os aplicativos que publicam eventos maiores que 64 quilobytes em um computador com Windows Server 2003, Windows XP ou Windows 2000 não poderão publicar eventos em um computador Windows Vista ou posterior.
