---
title: Escolhendo o modelo de threading
description: Escolhendo o modelo de threading
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1966a4b000683bb7549ce9c825051324088fd85c41146137443045785b5e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896506"
---
# <a name="choosing-the-threading-model"></a>Escolhendo o modelo de threading

Escolher o modelo de threading para um objeto depende da função do objeto. Um objeto que faz E/S extensiva pode dar suporte ao threading livre para fornecer resposta máxima aos clientes permitindo chamadas de interface durante a latência de E/S. Por outro lado, um objeto que interage com o usuário pode dar suporte ao apartment threading para sincronizar chamadas COM de entrada com suas operações de janela.

É mais fácil dar suporte ao apartment threading em apartments de thread único porque o COM fornece sincronização por chamada. O suporte ao thread livre é mais difícil porque o objeto deve implementar a sincronização; no entanto, a resposta aos clientes pode ser melhor porque a sincronização pode ser implementada para seções menores de código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando interfaces entre apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Multithreaded Apartments](multithreaded-apartments.md)
</dt> <dt>

[Problemas de threading de servidor em processo](in-process-server-threading-issues.md)
</dt> <dt>

[Processos, threads e apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicação multithread e single-threaded](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments de thread único](single-threaded-apartments.md)
</dt> </dl>

 

 




