---
title: Serviços de Serialização
description: O Microsoft RPC dá suporte a dois métodos para codificar e decodificar dados, coletivamente chamados de serialização de dados.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- RPC de Chamada de Procedimento Remoto , descrito, serialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54e6daf4ace5ffb3ee5d22886a570ae1e9ab1ae834cfac12a91d234c331e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035526"
---
# <a name="serialization-services"></a>Serviços de Serialização

O Microsoft RPC dá suporte a dois métodos para codificar e decodificar dados, coletivamente chamado *de serialização de dados*. Serialização significa que os dados são empacotados e desmarque dos buffers que você controla. Isso é diferente do uso tradicional de RPC, no qual os stubs e a biblioteca em tempo de executar RPC têm controle total dos buffers de marshaling e o processo é transparente. Você pode usar o buffer para armazenamento em mídia permanente, criptografia e assim por diante. Quando você codifica dados, os stubs RPC empacotam os dados para um buffer e passam o buffer para você. Ao decodificar dados, você fornece um buffer de marshaling com dados nele e os dados são desmarques do buffer para a memória. Você pode serializar com base em um procedimento ou tipo.

> [!Note]  
> O termo *selamento* é comumente usado entre desenvolvedores para descrever a serialização. Na verdade, os exemplos Windows SDK contém um diretório chamado *pickle* que preserva os programas de exemplo de serialização RPC.

 

A serialização aproveita os mecanismos RPC para marshaling e desmarque dados para outras finalidades. Por exemplo, em vez de usar várias operações de E/S para serializar um grupo de objetos em um fluxo, um aplicativo pode otimizar o desempenho serializando vários objetos de tipos diferentes em um buffer e, em seguida, escrevendo todo o buffer em uma única operação. As funções que manipulam identificador de serialização são independentes do tipo de serialização que você está usando.

Como outro exemplo, se você precisar usar um mecanismo de transporte de rede além de RPC, como Winsock (Soquetes Windows Microsoft). Com a serialização RPC, seu programa pode fazer chamadas para funções que realizarem marshal de seus dados em buffers e, em seguida, transmitir esses dados usando Winsock. Quando seu aplicativo recebe dados, ele pode usar o mecanismo de serialização RPC para desmarcar dados de buffers preenchidos pelas rotinas winsock. Isso oferece muitas das vantagens de aplicativos no estilo RPC e, ao mesmo tempo, permite que você use mecanismos de transporte não RPC.

Você também pode usar a serialização para fins não relacionados às comunicações de rede. Por exemplo, depois de usar as funções de codificação RPC para marshaling de dados para um buffer, você pode armazená-los em um arquivo para uso por outro aplicativo. Você também pode criptografá-lo. Você pode até mesmo usá-lo para armazenar uma representação independente de hardware e sistema operacional de dados em um banco de dados.

Os tópicos a seguir apresentam uma discussão sobre os serviços de serialização aos quais o Microsoft RPC dá suporte:

-   [Usando os Serviços de Serialização](using-serialization-services.md)
-   [Serialização de procedimento](procedure-serialization.md)
-   [Serialização de tipo](type-serialization.md)
-   [Alças de serialização](serialization-handles.md)

 

 




