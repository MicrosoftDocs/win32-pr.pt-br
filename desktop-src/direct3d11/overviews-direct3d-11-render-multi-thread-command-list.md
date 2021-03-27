---
title: Lista de comandos
description: Uma lista de comandos é uma sequência de comandos de GPU que podem ser gravados e reproduzidos. Uma lista de comandos pode melhorar o desempenho, reduzindo a quantidade de sobrecarga gerada pelo tempo de execução.
ms.assetid: 4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f8821645588ac7a9b48a4f6ce562c8c48cf96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636249"
---
# <a name="command-list"></a>Lista de comandos

Uma lista de comandos é uma sequência de comandos de GPU que podem ser gravados e reproduzidos. Uma lista de comandos pode melhorar o desempenho, reduzindo a quantidade de sobrecarga gerada pelo tempo de execução.

Use uma lista de comandos nos seguintes cenários:

-   Em um único quadro, renderize parte da cena em um thread durante a gravação de outra parte da cena em um segundo thread. No final do quadro, reproduza a lista de comandos gravada no primeiro thread. Use essa abordagem para dimensionar tarefas de renderização complexas em vários threads ou núcleos.
-   Pré-grave uma lista de comandos antes de precisar renderizá-la (por exemplo, enquanto um nível está carregando) e reproduza-a de forma eficiente mais tarde em sua cena. Essa otimização funciona bem quando você precisa renderizar algo com frequência.

Uma lista de comandos é imutável e é projetada para ser gravada e reproduzida durante uma única execução de um aplicativo. Uma lista de comandos não foi projetada para ser previamente registrada antes da execução do jogo e carregada a partir de sua mídia, pois não há como manter a lista.

Uma lista de comandos deve ser registrada por um contexto adiado, mas só pode ser reproduzida em um contexto imediato. Contextos adiados podem gerar listas de comandos simultaneamente.

-   Para registrar uma lista de comandos, consulte [como gravar uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md).
-   Para reproduzir uma lista de comandos, consulte [como: reproduzir uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md).
-   Ao usar uma lista de comandos, o desempenho depende da quantidade de suporte implementada em um driver. Para verificar o suporte ao driver, consulte [como: verificar o suporte do driver](overviews-direct3d-11-render-multi-thread-support.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização imediata e adiada](overviews-direct3d-11-render-multi-thread-render.md)
</dt> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




