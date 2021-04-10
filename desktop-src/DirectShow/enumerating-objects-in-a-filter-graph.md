---
description: Enumerando objetos em um grafo de filtro
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Enumerando objetos em um grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087568"
---
# <a name="enumerating-objects-in-a-filter-graph"></a>Enumerando objetos em um grafo de filtro

Um aplicativo pode precisar localizar um filtro específico no grafo de filtro ou até mesmo um PIN específico em um filtro. Por exemplo, ele pode usar uma interface que um filtro específico expõe. Ou, ele pode construir um grafo de filtro especializado e precisa chamar métodos em Pins individuais para conectar os filtros. Para essa finalidade, o DirectShow fornece vários métodos para enumerar objetos em um grafo de filtro.

Os enumeradores abordados nesta seção seguem o formulário padrão usado pelas interfaces de enumeração COM. Para obter mais informações, consulte o tópico "IEnumXXXX" no SDK da plataforma. Para obter informações sobre como enumerar filtros registrados no computador do usuário, mas ainda não estão no grafo de filtro, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).

Este artigo contém os seguintes tópicos:

-   [Enumerando filtros](enumerating-filters.md)
-   [Enumerando Pins](enumerating-pins.md)
-   [Enumerando tipos de mídia](enumerating-media-types.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



