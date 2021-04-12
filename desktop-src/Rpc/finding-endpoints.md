---
title: Localizando pontos de extremidade
description: Os programas de servidor escutam pontos de extremidade para solicitações de cliente. A sintaxe da cadeia de caracteres do ponto de extremidade depende da sequência de protocolo usada. Por exemplo, o ponto de extremidade para TCP/IP é um número de porta e a sintaxe de ponto de extremidade para pipes nomeados é um nome de pipe válido.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0a97df3408a4d3c24dff9de28553f9e4b2210d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294137"
---
# <a name="finding-endpoints"></a>Localizando pontos de extremidade

Os programas de servidor escutam pontos de extremidade para solicitações de cliente. A sintaxe da cadeia de caracteres do ponto de extremidade depende da sequência de protocolo usada. Por exemplo, o ponto de extremidade para TCP/IP é um número de porta e a sintaxe de ponto de extremidade para pipes nomeados é um nome de pipe válido.

Há dois tipos de pontos de extremidade: bem conhecidos e dinâmicos. Sua escolha de qual tipo de ponto de extremidade seu programa usa determina se o aplicativo distribuído ou a biblioteca de tempo de execução especifica o ponto de extremidade.

Esta seção aborda os pontos de extremidade e apresenta informações sobre como encontrá-los. Ele é organizado nos seguintes tópicos:

-   [Usando pontos de extremidade de Well-Known](#using-well-known-endpoints)
-   [Usando pontos de extremidade dinâmicos](#using-dynamic-endpoints)
-   [Exportando pontos de extremidade Well-Known para o banco de dados de mapa](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Os *pontos de extremidade estáticos* e os *pontos de extremidade bem conhecidos* são equivalentes e usados de maneira intercambiável.

 

É possível que seu aplicativo cliente use o mapa do ponto de extremidade para determinar se um programa de servidor está em execução no momento. O cliente pode chamar [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)e [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) para ver se o servidor registrou a interface específica necessária no mapa do ponto de extremidade.

## <a name="using-well-known-endpoints"></a>Usando pontos de extremidade conhecidos

Pontos de extremidade conhecidos são pontos de extremidade previamente atribuídos que o programa do servidor usa sempre que é executado. Como o servidor sempre ouve esse ponto de extremidade específico, o cliente sempre tenta se conectar a ele. Os pontos de extremidade bem conhecidos são geralmente atribuídos pela autoridade responsável pelo protocolo de transporte. Como os computadores host do servidor têm um número finito de pontos de extremidade disponíveis, os desenvolvedores de aplicativos são fortemente desencorajados de usar pontos de extremidade bem conhecidos. Outra vantagem dos pontos de extremidade dinâmicos é que eles simplificam o gerenciamento e a manutenção de longo prazo do sistema.

Um aplicativo distribuído pode especificar um ponto de extremidade bem conhecido em uma cadeia de caracteres e passar essa cadeia de caracteres como um parâmetro para a função [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). Como alternativa, a cadeia de caracteres do ponto de extremidade pode aparecer no cabeçalho da interface do arquivo IDL como parte do atributo da interface do \[ [ponto de extremidade](/windows/desktop/Midl/endpoint) \] .

Você pode usar duas abordagens para implementar o ponto de extremidade bem conhecido:

-   Especificar todas as informações em uma associação de cadeia de caracteres
-   Armazenar o ponto de extremidade conhecido no banco de dados do serviço de nome

Você pode gravar todas as informações necessárias para estabelecer uma ligação em um aplicativo distribuído ao desenvolvê-lo. O cliente pode especificar o ponto de extremidade conhecido diretamente em uma cadeia de caracteres, chamar [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para criar uma cadeia de caracteres que contém todas as informações de associação e fornecer essa cadeia de caracteres para a função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obter um identificador. O cliente e o servidor podem ser embutidos em código para usar um ponto de extremidade conhecido, ou escritos para que as informações do ponto de extremidade sejam provenientes da linha de comando, de um arquivo de dados, de um arquivo de configuração ou do arquivo IDL.

O aplicativo cliente também pode consultar um banco de dados de serviço de nome para obter informações conhecidas do ponto de extremidade.

## <a name="using-dynamic-endpoints"></a>Usando pontos de extremidade dinâmicos

O número de pontos de extremidade para um servidor específico e uma sequência de protocolo específica geralmente são limitados. Por exemplo, quando você usa a sequência de protocolo [ \_ \_ TCP IP ncacn](/windows/desktop/Midl/ncacn-ip-tcp) , indicando que a comunicação de rede RPC ocorre usando TCP/IP, apenas um número limitado de portas está disponível (a maioria dos sistemas tem apenas o intervalo de 1025 a 5000 aberto). As bibliotecas de tempo de execução RPC permitem atribuir pontos de extremidade dinamicamente, conforme necessário. Como o número de UUIDs de interface possíveis é praticamente ilimitado, usar o UUID de interface para direcionar a chamada oferece mais espaço para expansão e mais flexibilidade.

Por padrão, as funções de biblioteca de tempo de execução RPC pesquisam informações de ponto de extremidade quando consultam um banco de dados de serviço de nome. Se o ponto de extremidade for dinâmico, o banco de dados do serviço de nome não conterá informações de ponto de extremidade. No entanto, a consulta fornecerá ao seu programa cliente o nome de um servidor. Em seguida, ele pode pesquisar o mapa de ponto de extremidade do servidor.

Se o cliente precisar fazer uma chamada de procedimento remoto usando um ponto de extremidade dinâmico, o método preferencial será fazer a chamada em um identificador de associação parcialmente associado. O tempo de execução RPC resolve o ponto de extremidade de forma transparente. Esse método é superior ao uso da função [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) , pois permite mecanismos de cache avançados no tempo de execução de RPC.

Se for necessário um controle mais específico sobre a seleção de ponto de extremidade, os clientes poderão pesquisar o mapa de ponto de extremidade uma entrada por vez chamando as funções [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin), [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)e [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) .

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportando pontos de extremidade conhecidos para o banco de dados do mapa do ponto final

É possível misturar as duas abordagens para localizar pontos de extremidade, especialmente quando um sistema distribuído está fazendo a transição de um modelo de ponto de extremidades conhecido para um modelo de ponto de extremidade dinâmico. Nessas transições, uma versão intermediária do servidor usará um ponto de extremidade conhecido, mas também registrará o ponto de extremidade conhecido com o banco de dados do mapa do ponto de extremidade. Essa abordagem permite que clientes que usam um ponto de extremidade e clientes bem conhecidos que usam um ponto de extremidade dinâmico para se conectar. Depois que todos os servidores forem atualizados, uma nova versão do cliente poderá ser implantada que usa somente pontos de extremidade dinâmicos. Depois que todos os clientes são atualizados, uma versão final do servidor pode parar de usar pontos de extremidade bem conhecidos e começar a usar somente pontos de extremidade dinâmicos.

Essa abordagem permite um caminho de transição para aplicativos que começaram com um ponto de extremidade bem conhecido, mas que desejam migrar para um ponto de extremidade dinâmico sem exigir uma atualização simultânea de todos os servidores e clientes.

 

 