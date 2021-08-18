---
description: Quality-Control gerenciamento
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control gerenciamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824410b697a29ee73fc269748595fdcae91d054a161561b282536a05dcf92ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747706"
---
# <a name="quality-control-management"></a>Quality-Control gerenciamento

O controle de qualidade é um mecanismo para ajustar a taxa de fluxo de dados por meio do grafo de filtro em resposta ao desempenho em tempo de execução. Se um filtro de renderização estiver recebendo dados demais ou muito pouco, ele poderá enviar uma *mensagem de qualidade*. A mensagem de qualidade solicita um ajuste na taxa de dados. Por padrão, as mensagens de qualidade viajam upstream do renderador até alcançarem um filtro que pode responder (se for o caso). Um aplicativo também pode implementar um gerenciador de qualidade personalizado. Nesse caso, o renderdor passa mensagens de qualidade diretamente para o gerenciador de qualidade do aplicativo.

Este artigo contém os tópicos a seguir.

-   [Mensagens de qualidade](quality-messages.md)
-   [Controle de qualidade padrão](default-quality-control.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dados Flow para desenvolvedores de filtro](data-flow-for-filter-developers.md)
</dt> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



