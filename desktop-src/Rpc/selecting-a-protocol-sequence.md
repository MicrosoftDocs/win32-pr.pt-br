---
title: Selecionando uma sequência de protocolo
description: Uma sequência de protocolo é a linguagem que um sistema operacional de rede usa para falar pela rede com outros computadores.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005970"
---
# <a name="selecting-a-protocol-sequence"></a>Selecionando uma sequência de protocolo

Uma sequência de protocolo é a linguagem que um sistema operacional de rede usa para falar pela rede com outros computadores. Em termos mais específicos, os aplicativos RPC devem especificar uma cadeia de caracteres que representa uma combinação de um protocolo RPC, um protocolo de transporte e um protocolo de rede.

O Microsoft RPC dá suporte a três protocolos RPC:

-   Protocolo orientado a conexão da arquitetura de computação de rede (NCACN)
-   Protocolo de dataNCADG (arquitetura de computação de rede)
-   Chamada de procedimento remoto local de arquitetura de computação de rede (NCALRPC)

Os aplicativos RPC podem usar o protocolo NCALRPC para invocar procedimentos oferecidos por programas de servidor em execução no mesmo computador em que o programa cliente é executado. Isso é, de longe, o método mais eficiente para chamar a funcionalidade em um processo diferente no mesmo computador.

Os protocolos de rede e transporte que seu aplicativo usa dependem de quais protocolos a rede dá suporte. Muitas redes atualmente, incluindo a Internet, dão suporte a TCP/IP. Outros protocolos de rede e de transporte comuns são IPX/SPX, NetBIOS e DSP do AppleTalk. O Microsoft RPC dá suporte a esses e a outros protocolos de transporte e de rede. Para obter uma lista completa, consulte [constantes de sequência de protocolo](protocol-sequence-constants.md).

Quando seu aplicativo usa identificadores de ligação automática, ele não precisa especificar a sequência de protocolo. Se usar identificadores implícitos ou explícitos, ele deverá obter ou especificar a sequência de protocolo. Cada sistema distribuído deve examinar o ambiente no qual ele será implantado para determinar qual sequência de protocolo é mais adequada para esse ambiente.

Nem todas as sequências de protocolo têm funcionalidade equivalente. Os desenvolvedores devem verificar se a sequência de protocolo escolhida dá suporte aos recursos necessários. Em geral, **Ncalrpc** para comunicações locais e **ncacn \_ IP \_ TCP** ou **ncacn \_ http** para comunicações remotas são recomendadas; elas funcionam em todos os ambientes, têm desempenho ideal e oferecem suporte a todos os recursos de práticas recomendadas necessários.

Os clientes também podem especificar informações de sequência de protocolo que eles obtêm de Active Directory, o registro, as variáveis de ambiente criadas e inicializadas pelo programa de instalação, arquivos de configuração específicos do aplicativo ou cadeias de caracteres literais no código-fonte do programa.

Depois que o programa cliente tiver uma cadeia de caracteres de sequência de protocolo válida, ele poderá passar essas informações para as funções [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) e [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para criar o identificador de associação.

 

 




