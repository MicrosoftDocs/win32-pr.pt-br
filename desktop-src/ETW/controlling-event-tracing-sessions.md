---
description: As sessões de rastreamento de eventos registram eventos de um ou mais provedores.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controlando sessões de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970eb160812991677aac775af60d08458c269152edca4aa2e30cdf30c111d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130656"
---
# <a name="controlling-event-tracing-sessions"></a>Controlando sessões de rastreamento de eventos

As sessões de rastreamento de eventos registram eventos de um ou mais [provedores](providing-events.md). O controlador define a sessão e habilita os provedores. Definir a sessão normalmente inclui especificar o nome do arquivo de log e da sessão, o tipo de arquivo de log a ser usado e a resolução do carimbo de data/hora usado para registrar os eventos. Os controladores também podem atualizar e consultar sessões de rastreamento de eventos.

Os tópicos a seguir demonstram como definir e atualizar uma sessão e habilitar provedores de rastreamento de eventos:

-   [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)
-   [Configurando e iniciando uma sessão SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md)
-   [Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md)
-   [Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)
-   [Recuperando dados de rastreamento de eventos adicionais](retrieving-additional-event-tracing-data.md)

Para obter informações sobre como liberar e consultar sessões, consulte [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivamente.

Somente os usuários que executam com privilégios administrativos elevados, os usuários no grupo de usuários de log de desempenho e os aplicativos executados como LocalSystem, LocalService ou NetworkService podem controlar sessões de rastreamento de eventos. Para conceder a um usuário restrito a capacidade de controlar as sessões de rastreamento, adicione-as ao grupo de usuários de log de desempenho.

**Windows XP e Windows 2000:** Qualquer pessoa pode controlar uma sessão de rastreamento.

 

 
