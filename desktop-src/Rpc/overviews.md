---
title: Visões gerais
description: Página de navegação RPC (chamada de procedimento remoto) para obter as seções de visão geral.
ms.assetid: 49dc35c3-efd7-45a2-bec0-cd68ac150754
keywords:
- RPC de chamada de procedimento remoto, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea90c08dc075fdd90ae604b0d347ba6ac5baf9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292530"
---
# <a name="overviews"></a>Visões gerais

Essa parte do guia e da referência do programador de chamada de procedimento remoto (RPC) consiste em uma sequência de tópicos que o ajudarão a entender a programação de aplicativos distribuídos e o RPC da seguinte maneira:

-   O [modelo RPC da Microsoft](microsoft-rpc-model.md) fornece uma visão geral do modelo de programação cliente-servidor, padrões para programação de aplicativos distribuídos e uma descrição de como o Microsoft RPC funciona.
-   [A instalação do ambiente de programação RPC](installing-the-rpc-programming-environment.md) informa como instalar os arquivos e as ferramentas necessárias para desenvolver aplicativos distribuídos com o Microsoft RPC.
-   A [criação de aplicativos RPC](building-rpc-applications.md) descreve o compilador MIDL e o ambiente necessário para a criação de aplicativos distribuídos com o Microsoft RPC.
-   [Conectar o cliente e o servidor](connecting-the-client-and-the-server.md) fornece uma visão geral do processo de inicialização e execução de aplicativos distribuídos.
-   O [tutorial](tutorial.md) fornece uma visão geral do desenvolvimento de um pequeno aplicativo distribuído. Este exemplo demonstra todas as etapas do desenvolvimento de um aplicativo distribuído, as ferramentas que você usa e os componentes que compõem os programas executáveis.
-   Os [arquivos IDL e ACF](the-idl-and-acf-files.md) descrevem os arquivos IDL e ACF usados para especificar a interface para a chamada de procedimento remoto e as opções do compilador MIDL que controlam como esses arquivos são processados.
-   [Recursos de dados e linguagem](data-and-language-features.md) demonstra o uso de tipos de dados padrão.
-   [Matrizes e ponteiros](arrays-and-pointers.md) explica como passar ponteiros de matriz como parâmetros.
-   [Pipes](pipes.md) descreve como usar pipes nomeados como o mecanismo de transporte para chamadas de procedimento remoto.
-   [Associação e identificadores](binding-and-handles.md) descreve o identificador de associação — a estrutura de dados que permite ao desenvolvedor associar o aplicativo de chamada ao procedimento remoto.
-   O [Gerenciamento de memória](memory-management.md) oferece ideias sobre como gerenciar a memória no cliente e no servidor ao executar chamadas de procedimento remoto.
-   Os [serviços de serialização](serialization-services.md) descrevem os métodos de codificação ou decodificação de dados.
-   A [segurança](security.md) descreve os métodos para implementar recursos de segurança em seus aplicativos distribuídos.
-   [Instalar e configurar aplicativos RPC](installing-and-configuring-rpc-applications.md) discute a instalação de aplicativos de cliente e servidor, descreve como configurar o provedor de serviços de nome e o serviço de segurança. Esta seção também contém informações de transporte de rede para RPC.
-   O [RPC assíncrono](asynchronous-rpc.md) apresenta informações sobre as extensões assíncronas da Microsoft para a definição de RPC. As chamadas assíncronas de procedimento remoto retornam imediatamente sem aguardar a saída. Quando o procedimento remoto termina de executar no servidor, ele transfere dados de retorno para o cliente.
-   O [enfileiramento de mensagens RPC](rpc-message-queuing.md) descreve o uso do MSMQ (serviço de enfileiramento de mensagens), que permite que os usuários se comuniquem entre redes e sistemas, independentemente do estado atual dos aplicativos e sistemas de comunicação.
-   As [chamadas de procedimento remoto usando RPC sobre http](remote-procedure-calls-using-rpc-over-http.md) fornecem aos clientes RPC a capacidade de conectar-se com segurança pela Internet aos programas de servidor RPC e executar chamadas de procedimento remoto.
-   O [balanceamento de carga RPC](rpc-load-balancing.md) descreve a distribuição de grandes volumes de tráfego RPC sobre http entre vários servidores RPC em um farm de servidores.
-   Os [exemplos](examples.md) contêm uma descrição dos programas de RPC de exemplo fornecidos com o kit do desenvolvedor de software de plataforma Microsoft.

 

 




