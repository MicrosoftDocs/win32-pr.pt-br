---
title: Especificando sequências de protocolo
description: Os aplicativos de servidor devem selecionar uma ou mais sequências de protocolo para usar ao se comunicar com o cliente pela rede. A escolha das sequências de protocolo é dependente da rede. Consulte interpretando informações de associação e selecionando uma sequência de protocolo.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f43b8dc7b21fc2a6bebe98010b80dbf369ac96bb185cc75afa3b0a4f1acbba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925146"
---
# <a name="specifying-protocol-sequences"></a>Especificando sequências de protocolo

Os aplicativos de servidor devem selecionar uma ou mais sequências de protocolo para usar ao se comunicar com o cliente pela rede. A escolha das sequências de protocolo é dependente da rede. Consulte [interpretando informações de associação](interpreting-binding-information.md) e [selecionando uma sequência de protocolo](selecting-a-protocol-sequence.md).

O programa do servidor pode permitir que os clientes se conectem usando qualquer sequência de protocolo compatível com a rede. Para fazer isso, invoque [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) e passe \_ C \_ PROTSEQ \_ Max \_ requisitos \_ Default como o primeiro parâmetro. No entanto, essa não é a abordagem recomendada. Em vez disso, usar **Ncalrpc** para chamadas locais e **ncacn \_ IP \_ TCP** ou **ncacn \_ http** para chamadas remotas geralmente é suficiente. Redes heterogêneas são incomuns e praticamente todas as redes dão suporte a TCP/IP.

Se você quiser que o cliente restrinja a alocação de porta para pontos de extremidade dinâmicos para um intervalo de porta específico, chame [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) em vez disso. Essa função é específica para o Microsoft RPC e é extremamente útil para chamadas de procedimento remoto que passam por um firewall. Ele usa um parâmetro extra para passar sinalizadores de controle de alocação de porta para a função. Consulte [Configurando o registro para alocações de porta e Associação seletiva](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md).

Você pode especificar sequências de protocolo e informações de ponto de extremidade no arquivo MIDL ao desenvolver as interfaces do servidor. Se você fizer isso, o servidor deverá usar [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) para registrar todas as sequências de protocolo e as informações de ponto de extremidade associadas fornecidas no arquivo IDL. Além disso, há uma função [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) correspondente que também permite que o servidor passe a alocação de porta – sinalizadores de controle.

Se você quiser configurar seus programas de cliente e servidor para se comunicar com uma sequência de protocolo especificada, o aplicativo de servidor deverá chamar [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq). Para obter uma lista completa de sequências de protocolo RPC da Microsoft, consulte [constantes de sequência de protocolo](protocol-sequence-constants.md).

O Microsoft RPC também fornece [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) para permitir que os aplicativos selecionem sequências de protocolo específicas e controle a alocação de porta dinâmica.

Além dos protocolos orientados a conexão, o Microsoft RPC também dá suporte a protocolos de datagrama (sem conexão). Protocolos orientados a conexão são recomendados; os protocolos de datagrama têm conjuntos de recursos diferentes dos protocolos orientados a conexão e só devem ser usados se um desenvolvedor de sistema distribuído exigir um recurso disponível somente em protocolos de datagrama. Alguns dos recursos disponíveis ao usar os protocolos de datagrama são:

-   Os datagrams dão suporte aos protocolos de transporte sem conexão UDP e IPX.
-   Como não é necessário estabelecer e manter uma conexão, o Protocolo RPC de datagrama requer menos sobrecarga de recursos.
-   Os datagrams habilitam a vinculação mais rápida.
-   Assim como acontece com o RPC orientado a conexão, as chamadas RPC de datagrama são por padrão *nonidempotent*. Isso significa que a chamada tem a garantia de não ser executada mais de uma vez. No entanto, uma função pode ser marcada como idempotente no arquivo IDL informando ao RPC que é inofensiva executar a função mais de uma vez em resposta a uma única solicitação de cliente. Isso permite que o tempo de execução mantenha menos o estado no servidor. Observe que uma chamada idempotente seria executada novamente em raras circunstâncias em uma rede instável.
-   O datagrama RPC dá suporte ao atributo IDL de [difusão](/windows/desktop/Midl/broadcast) . A difusão permite que um cliente emita mensagens para vários servidores ao mesmo tempo. Isso permite que o cliente Localize um dos vários servidores disponíveis na rede ou controle vários servidores simultaneamente. Observe que a difusão de datagrama é válida somente dentro do link local e geralmente não cruza roteadores. As chamadas de difusão são implicitamente idempotentes. Se a chamada contiver parâmetros de \[ **saída** \] , somente a primeira resposta do servidor será retornada. Quando um servidor responde, todas as futuras RPCs sobre esse identificador de ligação serão enviadas somente para esse servidor, incluindo chamadas com o atributo de difusão. Para enviar outra difusão, crie um novo identificador de associação ou chame [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) no identificador existente.
-   O datagrama RPC dá suporte ao atributo [talvez](/windows/desktop/Midl/maybe) IDL. Isso permite que o cliente envie uma chamada para o servidor sem aguardar uma resposta ou confirmação. A chamada não pode conter parâmetros de \[ **saída** \] . Chamadas que usam **\[ as \]** chamadas If podem ser implicitamente idempotentes.

 

 