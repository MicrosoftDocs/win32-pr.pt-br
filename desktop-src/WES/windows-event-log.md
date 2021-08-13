---
title: Log de eventos do Windows
description: A API Windows log de eventos define o esquema que você usa para gravar um manifesto de instrumentação.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4306ce9722aba5b06109265c71cf387af2b35f63aef1cec070936400fff61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587191"
---
# <a name="windows-event-log"></a>Log de eventos do Windows

## <a name="purpose"></a>Finalidade

A API Windows log de eventos define o esquema que você usa para gravar um manifesto de instrumentação. Um manifesto de instrumentação identifica o provedor de eventos e os eventos que ele registra. A API também inclui as funções que um consumidor de eventos, como o [Visualizador de Eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), usaria para ler e renderizar os eventos. Para gravar os eventos definidos no manifesto, use as funções incluídas na API de ETW [(Rastreamento](/windows/desktop/ETW/event-tracing-portal) de Eventos).

Windows O Log de Eventos é o primeiro a ser a API de [Log](/windows/desktop/EventLog/event-logging) de Eventos que começa com o sistema operacional Windows Vista.

## <a name="developer-audience"></a>Público de desenvolvedores

Windows O Log de Eventos foi projetado para programadores C/C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Windows O Log de Eventos está incluído no sistema operacional a partir do Windows Vista e Windows Server 2008.

Para obter informações sobre os requisitos de tempo de executar para um elemento de programação específico, consulte a seção Requisitos da página de referência para esse elemento.

Para ver o histórico de versões completo, [consulte Novidades.](what-s-new.md)

## <a name="in-this-section"></a>Nesta seção


| Tópico                                                        | Descrição                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Usando Windows log de eventos](using-windows-event-log.md)        | Guia de procedimento que mostra como usar a API Windows log de eventos.                                 |
| [Windows Referência do Log de Eventos](windows-event-log-reference.md)| Os tipos de dados, funções, enumerações, estruturas, constantes e esquemas que a API inclui.|