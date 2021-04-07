---
title: Log de eventos do Windows
description: A API do log de eventos do Windows define o esquema que você usa para gravar um manifesto de instrumentação.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823974"
---
# <a name="windows-event-log"></a>Log de eventos do Windows

## <a name="purpose"></a>Finalidade

A API do log de eventos do Windows define o esquema que você usa para gravar um manifesto de instrumentação. Um manifesto de instrumentação identifica seu provedor de eventos e os eventos que ele registra. A API também inclui as funções que um consumidor de evento, como o [Visualizador de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), usaria para ler e renderizar os eventos. Para gravar os eventos definidos no manifesto, use as funções incluídas na API de [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW).

O log de eventos do Windows substitui a API de [log de eventos](/windows/desktop/EventLog/event-logging) que começa com o sistema operacional Windows Vista.

## <a name="developer-audience"></a>Público de desenvolvedores

O log de eventos do Windows foi projetado para programadores C/C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O log de eventos do Windows está incluído no sistema operacional a partir do Windows Vista e do Windows Server 2008.

Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

Para obter o histórico completo de versões, consulte [novidades](what-s-new.md).

## <a name="in-this-section"></a>Nesta seção


| Tópico                                                        | Descrição                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Usando o log de eventos do Windows](using-windows-event-log.md)        | Guia de procedimentos que mostra como usar a API do log de eventos do Windows.                                 |
| [Referência do log de eventos do Windows](windows-event-log-reference.md)| Os tipos de dados, as funções, as enumerações, as estruturas, as constantes e os esquemas que a API inclui.|