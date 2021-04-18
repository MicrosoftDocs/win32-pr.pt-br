---
title: Pipes (RPC)
description: O construtor de tipo de pipe é um mecanismo altamente eficiente para passar grandes quantidades de dados ou qualquer quantidade de dados que não esteja disponível na memória de uma só vez.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC de chamada de procedimento remoto, descrito, Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454532"
---
# <a name="pipes-rpc"></a>Pipes (RPC)

O construtor de tipo de pipe é um mecanismo altamente eficiente para passar grandes quantidades de dados ou qualquer quantidade de dados que não esteja disponível na memória de uma só vez. Usando um pipe, o tempo de execução de RPC lida com a transferência de dados real, eliminando a sobrecarga associada às chamadas repetidas de procedimento remoto.

Depois que um cliente chama um procedimento remoto que tem um parâmetro de pipe, o cliente e o servidor inserem loops para transferir dados. Os dados podem ser produzidos no cliente ou no servidor. De qualquer forma, a quantidade de dados (em bytes) não precisa ser conhecida com antecedência. Os dados podem ser produzidos ou consumidos incrementalmente. No loop de transferência de dados, o servidor chama rotinas de stub que carregam ou descarregam um buffer de dados. O cliente chama procedimentos definidos pelo programador para alocar buffers, carregar dados e descarregar dados dos buffers.

Esta seção fornece uma visão geral do uso de pipes para chamadas de procedimento remoto. Ele apresenta a visão geral dos seguintes tópicos:

-   [Terminologia de pipe essencial](essential-pipe-terminology.md)
-   [O estado do pipe](the-pipe-state.md)
-   [Definindo pipes em arquivos IDL](defining-pipes-in-idl-files.md)
-   [Implementação de pipe do lado do cliente](client-side-pipe-implementation.md)
-   [Implementação de pipe do lado do servidor](server-side-pipe-implementation.md)
-   [Regras para vários pipes](rules-for-multiple-pipes.md)
-   [Combinando parâmetros de pipe e nonpipe](combining-pipe-and-nonpipe-parameters.md)

Para obter mais informações sobre a sintaxe e as restrições do pipe, consulte [pipe](/windows/desktop/Midl/pipe) na referência da linguagem MIDL. O programa de exemplo de pipes no diretório de RPC dos exemplos do SDK (Software Development Kit) da plataforma \\ demonstra como usar os pipes **\[ out \]** para transferir dados entre um cliente e um servidor.

 

 
