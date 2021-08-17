---
description: Threads de streaming e o Gerenciador de Graph Filtro
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Threads de streaming e o Gerenciador de Graph Filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329766"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Threads de streaming e o Gerenciador de Graph Filtro

Quando o Gerenciador Graph Filtro interrompe o grafo, ele aguarda que todos os threads de streaming desliguem. Isso tem as seguintes implicações para filtros:

-   Um filtro nunca deve chamar métodos no Gerenciador Graph filtro de um thread de streaming.

    O Gerenciador Graph Filtro usa uma seção crítica para sincronizar suas próprias operações. Se um thread de streaming tentar manter essa seção crítica, ele poderá causar um deadlock. Por exemplo: suponha que outro thread pare o grafo. Esse thread usa o bloqueio de grafo de filtro e aguarda que o filtro pare de entregar dados. Se o filtro estiver aguardando o bloqueio, ele nunca será parar, causando um deadlock.

-   Um filtro nunca deve **AdicionarRef ou** **QueryInterface** o Gerenciador Graph filtro de um thread de streaming.

    Se o filtro tiver uma contagem de referência no Gerenciador Graph Filtro (por meio de **AddRef** ou **QueryInterface),** ele poderá se tornar o último objeto a manter uma contagem de referência. Quando o filtro chama **Release**, o Gerenciador Graph Filtros destrói a si mesmo. Dentro de sua rotina de limpeza, o Gerenciador Graph Filtro tenta parar o grafo, fazendo com que ele aguarde até que o thread de streaming saia. No entanto, ele está aguardando dentro do thread de streaming, portanto, o thread de streaming não pode sair. O resultado é um deadlock.

 

 



