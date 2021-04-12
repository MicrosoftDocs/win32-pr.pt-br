---
title: Escolhendo o modelo de Threading
description: Escolhendo o modelo de Threading
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364399"
---
# <a name="choosing-the-threading-model"></a>Escolhendo o modelo de Threading

Escolher o modelo de threading para um objeto depende da função do objeto. Um objeto que executa e/s extensiva pode dar suporte a Threading livre para fornecer o máximo de resposta aos clientes, permitindo chamadas de interface durante a latência de e/s. Por outro lado, um objeto que interage com o usuário pode dar suporte ao Threading Apartment para sincronizar chamadas COM de entrada com suas operações de janela.

É mais fácil oferecer suporte a Threading de apartamento em Apartments de thread único porque o COM fornece sincronização em uma base por chamada. O suporte ao Threading livre é mais difícil porque o objeto deve implementar a sincronização; no entanto, a resposta aos clientes pode ser melhor porque a sincronização pode ser implementada para seções menores de código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando interfaces em Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Apartments multithread](multithreaded-apartments.md)
</dt> <dt>

[Problemas de Threading do servidor em processo](in-process-server-threading-issues.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments de thread único](single-threaded-apartments.md)
</dt> </dl>

 

 




