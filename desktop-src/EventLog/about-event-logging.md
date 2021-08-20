---
description: Quando ocorre um erro, o administrador do sistema ou o representante de suporte deve determinar o que causou o erro, tentar recuperar todos os dados perdidos e impedir que o erro ocorra.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Sobre o log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9f30e4f8a44594b95215d748ac5cafda6b0633eefa668d0d864362c8f3c5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814253"
---
# <a name="about-event-logging"></a>Sobre o log de eventos

Quando ocorre um erro, o administrador do sistema ou o representante de suporte deve determinar o que causou o erro, tentar recuperar todos os dados perdidos e impedir que o erro ocorra. Será útil se os aplicativos, o sistema operacional e outros serviços do sistema registrarem eventos importantes, como condições de memória baixa ou tentativas excessivas de acessar um disco. O administrador do sistema pode usar o log de eventos para ajudar a determinar quais condições causaram o erro e identificar o contexto no qual ele ocorreu. Ao exibir periodicamente o log de eventos, o administrador do sistema pode ser capaz de identificar problemas (como um disco rígido com falha) antes de causar danos.

> [!Note]  
> A API de Log de Eventos foi projetada para aplicativos executados no sistema operacional Windows Server 2003, Windows XP ou Windows 2000. No Windows Vista, a infraestrutura de registro em log de eventos foi reprojetada. Os aplicativos projetados para executar no Windows Vista ou sistemas operacionais posteriores agora devem usar Windows Log de [Eventos](/windows/desktop/WES/windows-event-log) para registrar eventos.

 
Esta seção discute a interface de programação para escrever e consumir eventos usando o Log de Eventos.

-   [Tipos de evento](event-types.md)
-   [Diretrizes de registro em log](logging-guidelines.md)
-   [Elementos de log de eventos](event-logging-elements.md)
-   [Operações de registro em log de eventos](event-logging-operations.md)
-   [Modelo de registro em log de eventos](event-logging-model.md)
-   [Segurança do log de eventos](event-logging-security.md)

> [!Note]  
> Aplicativos que publicam eventos maiores que 64 quilobytes em um computador do Windows Server 2003, Windows XP ou Windows 2000 não poderão publicar eventos em um computador Windows Vista ou posterior.
