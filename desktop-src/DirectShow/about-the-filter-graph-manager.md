---
description: Sobre o Gerenciador de Graph Filtro
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Sobre o Gerenciador de Graph Filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ce7c9c9af137853efba501cace7680b533c13994a559102fd08dc48efa2076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074860"
---
# <a name="about-the-filter-graph-manager"></a>Sobre o Gerenciador de Graph Filtro

O [Gerenciador Graph Filtro é](filter-graph-manager.md) um objeto COM que controla os filtros em um grafo de filtro. Ele executa muitas funções, incluindo as seguintes:

-   Coordenar alterações de estado entre os filtros.
-   Estabelecer um relógio de referência.
-   Comunicando eventos de volta ao aplicativo.
-   Fornecendo métodos para aplicativos criarem o grafo de filtro.

Cada uma dessas funções é descrita brevemente aqui. Os detalhes podem ser encontrados em outro lugar na documentação.

**O estado altera**. As alterações de estado em filtros devem ocorrer em uma ordem específica. Portanto, o aplicativo não em emitido comandos de alteração de estado diretamente para os filtros. Em vez disso, ele fornece um único comando para o Gerenciador Graph Filtro, que distribui o comando para cada um dos filtros. A busca funciona de maneira semelhante: o aplicativo fornece um comando seek para o Gerenciador Graph Filtro, que o distribui para os filtros.

**Relógio de referência**. Todos os filtros no grafo usam o mesmo relógio, chamado de relógio *de referência*. O relógio de referência garante que todos os fluxos sejam sincronizados. A hora em que uma amostra de áudio ou quadro de vídeo deve ser renderizada é chamada de hora *de apresentação.* O tempo de apresentação é medido em relação ao relógio de referência. O Gerenciador Graph Filtro escolhe um relógio de referência, geralmente o relógio na placa de som ou o relógio do sistema.

**Graph eventos**. O Gerenciador Graph Filtro usa uma fila de eventos para informar a aplicação de eventos que ocorrem no grafo de filtro. Esse mecanismo é semelhante a um loop Windows mensagem.

**Graph de criação de dados**. O Gerenciador Graph Filtro fornece métodos para o aplicativo adicionar filtros ao grafo, conectar filtros a outros filtros e desconectar filtros.

Uma função que o Gerenciador Graph Filtro não trata é mover dados de um filtro para o próximo. Isso é feito pelos próprios filtros, por meio de suas conexões de pino. O processamento sempre acontece em um thread separado.

> [!Note]  
> Os filtros são sempre de thread livre, residem no mesmo processo que o Gerenciador Graph Filtro e são carregados de servidores em processo. Portanto, as chamadas de método não têm marshal entre filtros ou entre filtros e o Gerenciador Graph Filtro.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dados Flow no filtro Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Definindo o Graph relógio](setting-the-graph-clock.md)
</dt> <dt>

[Hora e relógios em DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



