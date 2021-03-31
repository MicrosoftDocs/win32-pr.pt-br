---
title: Serviços de serialização
description: O Microsoft RPC dá suporte a dois métodos de codificação e decodificação de dados, coletivamente chamados de dados de serialização.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- Chamada de procedimento remoto RPC, descrita, serialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636916"
---
# <a name="serialization-services"></a>Serviços de serialização

O Microsoft RPC dá suporte a dois métodos de codificação e decodificação de dados, coletivamente chamados de *dados de serialização*. A serialização significa que os dados são empacotados e desempacotados de buffers que você controla. Isso é diferente do uso tradicional de RPC, no qual os stubs e a biblioteca de tempo de execução RPC têm controle total sobre os buffers de marshaling e o processo é transparente. Você pode usar o buffer para armazenamento em mídia permanente, criptografia e assim por diante. Ao codificar dados, os stubs RPC realizam marshaling dos dados para um buffer e passam o buffer para você. Ao decodificar dados, você fornece um buffer de marshaling com dados e os dados são desempacotados do buffer para a memória. Você pode serializar um procedimento ou base de tipo.

> [!Note]  
> A *escolha* do termo é normalmente usada entre os desenvolvedores para descrever a serialização. Na verdade, os exemplos de SDK do Windows contêm um diretório chamado *pickle* que preserva os programas de exemplo de serialização RPC.

 

A serialização aproveita os mecanismos de RPC para marshaling e desempacotamento de dados para outros fins. Por exemplo, em vez de usar várias operações de e/s para serializar um grupo de objetos em um fluxo, um aplicativo pode otimizar o desempenho ao serializar vários objetos de diferentes tipos em um buffer e, em seguida, gravar o buffer inteiro em uma única operação. As funções que manipulam os identificadores de serialização são independentes do tipo de serialização que você está usando.

Como outro exemplo, se você precisar usar um mecanismo de transporte de rede além do RPC, como o Microsoft Windows Sockets (Winsock). Com a serialização RPC, seu programa pode fazer chamadas para funções que realizam marshaling dos dados em buffers e, em seguida, transmitem esses dados usando o Winsock. Quando seu aplicativo recebe dados, ele pode usar o mecanismo de serialização RPC para desempacotar dados de buffers preenchidos pelas rotinas do Winsock. Isso fornece muitas das vantagens dos aplicativos em estilo RPC e, ao mesmo tempo, permite que você use mecanismos de transporte não RPC.

Você também pode usar a serialização para fins não relacionados a comunicações de rede. Por exemplo, depois de usar as funções de codificação RPC para realizar marshaling de dados em um buffer, você pode armazená-los em um arquivo para uso por outro aplicativo. Você também pode criptografá-lo. Você pode até mesmo usá-lo para armazenar uma representação de dados independente do sistema operacional e de hardware em um banco de dado.

Os tópicos a seguir apresentam uma discussão dos serviços de serialização aos quais o Microsoft RPC dá suporte:

-   [Usando serviços de serialização](using-serialization-services.md)
-   [Serialização de procedimento](procedure-serialization.md)
-   [Serialização de tipo](type-serialization.md)
-   [Identificadores de serialização](serialization-handles.md)

 

 




