---
description: Threads de streaming e o Gerenciador de gráfico de filtro
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Threads de streaming e o Gerenciador de gráfico de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759111"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Threads de streaming e o Gerenciador de gráfico de filtro

Quando o Gerenciador de gráfico de filtro para o grafo, ele aguarda que todos os threads de streaming sejam desligados. Isso tem as seguintes implicações para filtros:

-   Um filtro nunca deve chamar métodos no Gerenciador do grafo de filtro de um thread de streaming.

    O Gerenciador de gráfico de filtro usa uma seção crítica para sincronizar suas próprias operações. Se um thread de streaming tentar manter essa seção crítica, isso poderá causar um deadlock. Por exemplo: Suponha que outro thread interrompa o grafo. Esse thread pega o bloqueio do grafo de filtro e aguarda o filtro parar de entregar os dados. Se o filtro estiver aguardando o bloqueio, ele nunca será interrompido, causando um deadlock.

-   Um filtro nunca deve ser **AddRef** ou **QueryInterface** no Gerenciador do grafo de filtro de um thread de streaming.

    Se o filtro mantiver uma contagem de referência no Gerenciador de gráfico de filtro (por meio de **AddRef** ou **QueryInterface**), ele poderá se tornar o último objeto para manter uma contagem de referência. Quando o filtro chama **Release**, o Gerenciador do grafo de filtro se destrói. Dentro de sua rotina de limpeza, o Gerenciador do grafo de filtro tenta parar o grafo, fazendo com que ele aguarde até que o thread de streaming saia. No entanto, ele está aguardando dentro do thread de streaming, portanto, o thread de streaming não pode sair. O resultado é um deadlock.

 

 



