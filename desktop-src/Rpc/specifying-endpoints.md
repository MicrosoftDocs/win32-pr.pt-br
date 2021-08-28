---
title: Especificando pontos de extremidade
description: Especificando pontos de extremidade bem conhecidos e dinâmicos na RPC (chamada de procedimento remoto).
ms.assetid: fc39b527-11e6-45a7-b3b5-8bcf469633d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff73f13f752e42917353a217f5a2fcfa8d1fcfa9dc60edf585c42d72b0d306e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017606"
---
# <a name="specifying-endpoints"></a>Especificando pontos de extremidade

Um ponto de extremidade é um endereço específico da rede de um processo do servidor para chamadas de procedimento remoto. O nome real do ponto de extremidade depende da sequência de protocolo usada. Por exemplo, TCP, UDP e HTTP usam portas. Pipes nomeados usam um nome de pipe nomeado. Aplicativos cliente/servidor podem usar um ponto de extremidade conhecido ou um ponto de extremidade dinâmico. Esta seção apresenta as técnicas que os programas de servidor usam para especificar pontos de extremidade bem conhecidos e dinâmicos. As informações são discutidas nos seguintes tópicos:

-   [Especificando pontos de extremidade conhecidos](#specifying-well-known-endpoints)
-   [Especificando pontos de extremidade dinâmicos](#specifying-dynamic-endpoints)

## <a name="specifying-well-known-endpoints"></a>Especificando pontos de extremidade conhecidos

Quando o servidor usa um ponto de extremidade conhecido, ele pode incluir os dados do ponto de extremidade como parte de sua entrada de banco de dado de serviço de nome. Se tiver, o identificador de associação do cliente conterá um endereço de servidor completo que inclui o ponto de extremidade conhecido quando o cliente importar o identificador de associação da entrada do servidor.

O programa de servidor também pode especificar pontos de extremidade bem conhecidos ao mesmo tempo em que especifica seqüências de protocolo. Invoque a função [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) ou [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) . A diferença entre os dois é que a última função tem um parâmetro extra que seu servidor pode usar para controlar a alocação de porta dinâmica.

Se o seu programa de servidor especificar suas informações de ponto de extremidade dessa forma, ele também deverá chamar a função [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) para registrar o ponto de extremidade no mapa do ponto de extremidade. Embora o ponto de extremidade seja sempre o mesmo, o cliente pode usar o mapa do ponto de extremidade para localizar o servidor.

Como as sequências de protocolo, um aplicativo pode especificar informações de ponto de extremidade em seu arquivo IDL. Quando ele faz isso, ele deve registrar as sequências de protocolo e os pontos de extremidade ao mesmo tempo invocando a função [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) ou [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) . Nesse caso, o cliente tem acesso às informações do ponto de extremidade por meio da especificação da interface no arquivo IDL. Portanto, não é necessário chamar a função [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) .

## <a name="specifying-dynamic-endpoints"></a>Especificando pontos de extremidade dinâmicos

Um ponto de extremidade dinâmico é um ponto de extremidade que o computador host do servidor atribui quando o servidor começa a execução. A maioria dos aplicativos de servidor usa pontos de extremidade dinâmicos para evitar conflitos com outros programas em relação ao número limitado de portas que estão disponíveis no sistema de computador host do servidor. No entanto, os programas que usam pipes nomeados ou a sequência de protocolo [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) têm um espaço de nome de ponto de extremidade muito grande. Eles se beneficiam menos de pontos de extremidade dinâmicos do que programas usando outros transportes.

Os programas de servidor registram pontos de extremidade dinâmicos em um banco de dados de mapa de ponto de Se você quiser que o servidor use qualquer ponto de extremidade disponível, chame [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex), [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) ou [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex). Isso define a biblioteca de tempo de execução RPC para usar todas ou uma sequência de protocolo válida com pontos de extremidade dinâmicos. O servidor deve então chamar [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obter um conjunto de identificadores de associação válidos. O servidor passa o conjunto de identificadores de associação, ou o vetor de associação, para a função [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) para registrar todos os pontos de extremidade adequados no mapa de Endpoint. Para cada chamada que o servidor faz para **RpcEpRegister**, deve haver uma chamada correspondente para [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) para liberar a memória que o vetor de associação usa.

Observe que os programas de servidor podem usar a função [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) em vez de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister). Os programas normalmente usam **RpcEpRegisterNoReplace** quando várias cópias de um programa de servidor devem ser executadas em um sistema host de servidor.

As funções [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) e [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) adicionam as interfaces do servidor e os identificadores de associação ao banco de dados do mapeador de ponto de extremidade. Quando o cliente faz uma chamada de procedimento remoto usando um identificador parcialmente associado, a biblioteca de tempo de execução do cliente solicita ao mapeador de ponto de extremidade do computador do servidor o ponto de extremidade de uma instância de servidor compatível. A biblioteca de cliente fornece o UUID de interface, a sequência de protocolo e, se presente, o UUID de objeto no identificador de associação de cliente. O mapeador de ponto de extremidade procura uma entrada de banco de dados que corresponda às informações do cliente. O UUID da interface de cliente/servidor, a versão principal da interface e a sequência de protocolo devem corresponder exatamente. Além disso, a versão secundária da interface do servidor deve ser maior ou igual à versão secundária do cliente.

Se todos os testes forem bem-sucedidos, o mapeador de ponto de extremidade retornará o ponto de extremidade válido e a biblioteca de tempo de execução do cliente atualizará o ponto de extremidade no identificador de associação.

Os pontos de extremidade dinâmicos são limpos automaticamente do banco de dados mapeador de pontos de extremidades quando o processo do servidor para de ser executado. Você pode remover o ponto de extremidade do banco de dados do mapeador de ponto de extremidade antes de o programa de servidor sair usando a função [**RpcEpUnregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepunregister) ou pode permitir que a limpeza automática gerencie a remoção do ponto de extremidade.

 

 