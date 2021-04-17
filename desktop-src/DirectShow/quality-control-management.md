---
description: Gerenciamento de Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gerenciamento de Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758832"
---
# <a name="quality-control-management"></a>Gerenciamento de Quality-Control

O controle de qualidade é um mecanismo para ajustar a taxa de fluxo de dados por meio do grafo de filtro em resposta ao desempenho em tempo de execução. Se um filtro de processador estiver recebendo muitos dados ou poucos dados, ele poderá enviar uma *mensagem de qualidade*. A mensagem de qualidade solicita um ajuste na taxa de dados. Por padrão, as mensagens de qualidade viajam para upstream a partir do renderizador até chegarem a um filtro que pode responder (se houver). Um aplicativo também pode implementar um Gerenciador de qualidade personalizado. Nesse caso, o renderizador passa mensagens de qualidade diretamente para o Gerenciador de qualidade do aplicativo.

Este artigo contém os tópicos a seguir.

-   [Mensagens de qualidade](quality-messages.md)
-   [Controle de qualidade padrão](default-quality-control.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md)
</dt> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



