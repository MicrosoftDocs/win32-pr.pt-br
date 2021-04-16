---
description: Sobre o Gerenciador do grafo de filtro
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Sobre o Gerenciador do grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500597"
---
# <a name="about-the-filter-graph-manager"></a>Sobre o Gerenciador do grafo de filtro

O [Gerenciador do grafo de filtro](filter-graph-manager.md) é um objeto com que controla os filtros em um grafo de filtro. Ele executa muitas funções, incluindo as seguintes:

-   Coordenando alterações de estado entre os filtros.
-   Estabelecendo um relógio de referência.
-   Comunicação de eventos de volta para o aplicativo.
-   Fornecer métodos para que os aplicativos criem o gráfico de filtro.

Cada uma dessas funções é descrita brevemente aqui. Os detalhes podem ser encontrados em outro lugar na documentação.

**Alterações de estado**. As alterações de estado dentro dos filtros devem ocorrer em uma ordem específica. Portanto, o aplicativo não emite comandos de alteração de estado diretamente para os filtros. Em vez disso, ele fornece um único comando para o Gerenciador do grafo de filtro, que distribui o comando para cada um dos filtros. Procurar funciona de maneira semelhante: o aplicativo fornece um comando de busca para o Gerenciador do grafo de filtro, que o distribui para os filtros.

**Relógio de referência**. Todos os filtros no grafo usam o mesmo relógio, chamado de relógio de *referência*. O relógio de referência garante que todos os fluxos sejam sincronizados. A hora em que um quadro de vídeo ou amostra de áudio deve ser renderizado é chamada de *tempo de apresentação*. O tempo de apresentação é medido em relação ao relógio de referência. O Gerenciador de gráfico de filtro escolhe um relógio de referência, geralmente o relógio na placa de som ou o relógio do sistema.

**Eventos de grafo**. O Gerenciador de gráfico de filtro usa uma fila de eventos para informar a aplicação de eventos que ocorrem no grafo de filtro. Esse mecanismo é semelhante a um loop de mensagem do Windows.

**Métodos de criação de gráficos**. O Gerenciador de gráfico de filtro fornece métodos para que o aplicativo adicione filtros ao grafo, conecte filtros a outros filtros e desconecte filtros.

Uma função que o Gerenciador de gráfico de filtro não trata é mover dados de um filtro para o próximo. Isso é feito pelos filtros em si, por meio de suas conexões de PIN. O processamento sempre acontece em um thread separado.

> [!Note]  
> Os filtros são sempre de thread livre, residem no mesmo processo que o Gerenciador do grafo de filtro e são carregados de servidores em processo. Portanto, as chamadas de método não são empacotadas entre filtros ou entre filtros e o Gerenciador de gráfico de filtro.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Configurando o relógio do grafo](setting-the-graph-clock.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



