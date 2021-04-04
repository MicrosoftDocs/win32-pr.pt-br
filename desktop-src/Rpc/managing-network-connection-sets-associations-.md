---
title: Gerenciando conjuntos de conexões de rede (associações)
description: A partir do Windows 2000, o tempo de execução do RPC pode manter mais de uma conexão entre o cliente e o servidor.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Gerenciando conjuntos de conexões de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e99afe23d90e44d85dc7a2ec9301b45e1f20b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160168"
---
# <a name="managing-network-connection-sets-associations"></a>Gerenciando conjuntos de conexões de rede (associações)

A partir do Windows 2000, o tempo de execução do RPC pode manter mais de uma conexão entre o cliente e o servidor. Isso facilita a operação em transportes que não dão suporte à alteração da identidade do cliente sem restabelecer a conexão, clientes multithread e clientes assíncronos. O conjunto de conexões entre um processo de cliente e um ponto de extremidade do servidor é chamado de *Associação* na terminologia do RPC. Entender as associações pode melhorar a implementação do RPC.

Em um cenário de identidade de único thread, de cliente único, o RPC abre uma conexão entre um processo de cliente e um ponto de extremidade do servidor para fazer chamadas RPC. Quando uma chamada RPC síncrona é feita, o cliente envia a solicitação ao servidor nessa conexão e também recebe a resposta nela. Quando o número de threads que fazem chamadas RPC no processo do cliente aumenta, a identidade de segurança do cliente pode ser alterada. Quando as chamadas assíncronas/de pipe são misturadas com chamadas síncronas no cliente, a RPC pode precisar de mais de uma conexão de rede. Todas as conexões no conjunto são colocadas em um pool de conexões chamado associação.

Uma chamada de procedimento remoto síncrona usa exclusivamente uma determinada conexão para estar em conformidade com os padrões de RPC. Uma conexão usada por uma chamada RPC síncrona será considerada ocupada se uma solicitação tiver sido enviada, mas uma resposta não tiver sido recebida. Nenhum outro tráfego é permitido nessa conexão até que a resposta seja recebida. O tempo de execução de RPC tenta multiplexar chamadas de RPC assíncronas e de pipe na mesma conexão. Chamadas síncronas e assíncronas/de pipe não podem ser misturadas na mesma conexão, o que significa que uma determinada conexão pode ser usada para chamadas RPC síncronas ou para chamadas RPC assíncronas/de pipe.

O RPC tenta agressivamente a reutilização de conexões do pool. Quando uma nova chamada RPC é feita, o RPC tenta encontrar uma conexão adequada do pool e cria uma nova conexão somente se uma conexão adequada não puder ser encontrada. Para que uma conexão seja considerada adequada, ela deve:

-   Ser do tipo apropriado (síncrono ou assíncrono/pipe).
-   Seja gratuito.
-   Ter a mesma identidade de segurança que o identificador de associação no qual a chamada é feita. Se o controle de identidade dinâmico for usado, a identidade do identificador de associação será atualizada a partir do token de thread no início da chamada. Se o rastreamento de identidade estático for usado, a identidade do cliente carimbada no identificador de associação será usada.

Quando a chamada for concluída, quando a resposta for recebida, a conexão será marcada como livre e poderá ser usada para outras chamadas RPC.

A identidade de segurança em uma conexão não pode ser alterada. Por exemplo, se um grande número de chamadas para o mesmo servidor for feito sob diferentes identidades de segurança, o número de conexões no pool de threads aumentará. A associação em si é de referência-contada e, quando todas as referências forem canceladas, ela parará e fechará todas as conexões. Cada identificador de associação e cada manipulador de contexto mantêm uma referência na associação. Quando todos são fechados, a associação desaparece. No Windows XP, as associações não necessariamente desaparecem imediatamente; Eles podem permanecer por um curto período (o período de destino é de 20 segundos, mas o tempo de execução RPC pode optar por atrasar a destruição da Associação se nenhum thread estiver disponível para executar a tarefa). Se você não quiser que a associação fique ativa depois que o último identificador de contexto/identificador de associação for fechado, use \_ a \_ opção RPC C opt não \_ \_ persistente para forçar o tempo de execução RPC a fechar imediatamente a conexão.

 

 




