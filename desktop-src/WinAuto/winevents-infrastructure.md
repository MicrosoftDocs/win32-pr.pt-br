---
title: Infraestrutura de WinEvents
description: O sistema operacional Microsoft Windows inclui um recurso, chamado WinEvents, que permite que processos e aplicativos em execução na área de trabalho do Windows troquem determinados tipos de informações.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103639076"
---
# <a name="winevents"></a>WinEvents

O sistema operacional Microsoft Windows inclui um recurso, chamado *WinEvents*, que permite que processos e aplicativos em execução na área de trabalho do Windows troquem determinados tipos de informações. As ferramentas de acessibilidade que usam a automação da interface do usuário da Microsoft e o Microsoft Acessibilidade Ativa estão entre os usuários primários do WinEvents.

No contexto de acessibilidade, os provedores de automação da interface do usuário e os Microsoft Acessibilidade Ativa Servers usam WinEvents para notificar os clientes sobre alterações em uma interface do usuário do aplicativo, como quando um elemento de interface do usuário foi criado ou destruído, ou quando um nome de elemento, estado ou valor foi alterado.

Esta seção fornece sugestões, diretrizes e exemplos para ajudar os clientes a lidar com o WinEvents e para ajudar os servidores a determinar quando disparar o WinEvent apropriado.

## <a name="in-this-section"></a>Nesta seção

-   [O que são WinEvents?](what-are-winevents.md)
-   [Registrando uma função de gancho](registering-a-hook-function.md)
-   [Eventos de nível de sistema e Object-Level](system-level-and-object-level-events.md)
-   [Funções de gancho in-context e out-of-Context](in-context-and-out-of-context-hook-functions.md)
-   [Proteção contra reentrância em funções de Hook](guarding-against-reentrancy-in-hook-functions.md)
-   [Alocação de IDs WinEvent](allocation-of-winevent-ids.md)

Para obter uma visão geral do processo de notificação de eventos no Microsoft Acessibilidade Ativa, consulte [WinEvents](winevents-overview.md) na [visão geral técnica](technical-overview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Infraestrutura comum](common-infrastructure.md)
</dt> </dl>

 

 




