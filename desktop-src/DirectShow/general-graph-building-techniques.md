---
description: Técnicas de Graph-Building geral
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Técnicas de Graph-Building geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163702"
---
# <a name="general-graph-building-techniques"></a>Técnicas de Graph-Building geral

Cada aplicativo do DirectShow começa com a criação de um grafo de filtro. Ao ler os tópicos de visão geral na documentação do DirectShow, você descobrirá que a maioria começa descrevendo o tipo de grafo de filtro necessário. Em alguns casos, há um método ou um objeto auxiliar especificamente projetado para a criação desse tipo de grafo. Por exemplo, o objeto do [Construtor de gráficos de DVD](dvd-graph-builder.md) cria grafos de reprodução de DVD. Em outros casos, o aplicativo deve construir o grafo adicionando filtros e conectando-os.

Esta seção apresenta algumas funções auxiliares que implementam operações básicas de criação de gráficos. Eles podem ser usados por qualquer aplicativo do DirectShow que precise criar ou modificar um gráfico de filtro. Esta seção contém os seguintes tópicos:

-   [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md)
-   [Localizar um PIN não conectado em um filtro](find-an-unconnected-pin-on-a-filter.md)
-   [Conectar dois filtros](connect-two-filters.md)
-   [Localizar uma interface em um filtro ou PIN](find-an-interface-on-a-filter-or-pin.md)
-   [Localizar o par de um filtro](find-a-filters-peer.md)
-   [Remover todos os filtros no grafo](remove-all-the-filters-in-the-graph.md)
-   [Criando gráficos com o construtor de grafo de captura](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Enumerando dispositivos e filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Conexão inteligente](intelligent-connect.md)
</dt> </dl>

 

 



