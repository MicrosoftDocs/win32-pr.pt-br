---
title: Localizar pontos de extremidade
description: Os programas de servidor escutam os pontos de extremidade para solicitações do cliente. A sintaxe da cadeia de caracteres do ponto de extremidade depende da sequência de protocolo que você usa. Por exemplo, o ponto de extremidade para TCP/IP é um número da porta e a sintaxe do ponto de extremidade para pipes nomeados é um nome de pipe válido.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024a85704287db7e5f78bb67eee9b64a7c6dc84ce5724623450d36f743e5fa9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021276"
---
# <a name="finding-endpoints"></a>Localizar pontos de extremidade

Os programas de servidor escutam os pontos de extremidade para solicitações do cliente. A sintaxe da cadeia de caracteres do ponto de extremidade depende da sequência de protocolo que você usa. Por exemplo, o ponto de extremidade para TCP/IP é um número da porta e a sintaxe do ponto de extremidade para pipes nomeados é um nome de pipe válido.

Há dois tipos de pontos de extremidade: bem conhecidos e dinâmicos. Sua escolha de qual tipo de ponto de extremidade seu programa usa determina se o aplicativo distribuído ou a biblioteca em tempo de executar especifica o ponto de extremidade.

Esta seção aborda os pontos de extremidade e apresenta informações sobre como encontrá-los. Ele é organizado nos seguintes tópicos:

-   [Usando Well-Known pontos de extremidade](#using-well-known-endpoints)
-   [Usando pontos de extremidade dinâmicos](#using-dynamic-endpoints)
-   [Exportando Well-Known pontos de extremidade para o banco de dados de mapa de ponto de extremidade](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Os termos *pontos de extremidade estáticos* e pontos de extremidade conhecidos são *equivalentes* e usados de forma intercambiável.

 

É possível que o aplicativo cliente use o mapa do ponto de extremidade para determinar se um programa de servidor está em execução no momento. Seu cliente pode chamar [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)e [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) para ver se o servidor registrou a interface específica necessária no mapa do ponto de extremidade.

## <a name="using-well-known-endpoints"></a>Usando pontos de extremidade conhecidos

Pontos de extremidade conhecidos são pontos de extremidade pré-atribuídos que o programa de servidor usa sempre que é executado. Como o servidor sempre escuta esse ponto de extremidade específico, o cliente sempre tenta se conectar a ele. Os pontos de extremidade conhecidos geralmente são atribuídos pela autoridade responsável pelo protocolo de transporte. Como os computadores host do servidor têm um número finito de pontos de extremidade disponíveis, os desenvolvedores de aplicativos não são fortemente desencorajados de usar pontos de extremidade conhecidos. Outra vantagem dos pontos de extremidade dinâmicos é que eles simplificam o gerenciamento e a manutenção de longo prazo do sistema.

Um aplicativo distribuído pode especificar um ponto de extremidade conhecido em uma cadeia de caracteres e passar essa cadeia de caracteres como um parâmetro para a função [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). Como alternativa, a cadeia de caracteres do ponto de extremidade pode aparecer no header da interface de arquivo IDL como parte do atributo \[ [de](/windows/desktop/Midl/endpoint) interface do \] ponto de extremidade.

Você pode usar duas abordagens para implementar o ponto de extremidade conhecido:

-   Especificar todas as informações em uma associação de cadeia de caracteres
-   Armazenar o ponto de extremidade conhecido no nome do banco de dados de serviço

Você pode gravar todas as informações necessárias para estabelecer uma associação em um aplicativo distribuído ao desenvolvê-la. O cliente pode especificar o ponto de extremidade conhecido diretamente em uma cadeia de caracteres, chamar [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para criar uma cadeia de caracteres que contém todas as informações de associação e fornecer essa cadeia de caracteres à função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obter um handle. O cliente e o servidor podem ser codificados para usar um ponto de extremidade conhecido ou gravados para que as informações do ponto de extremidade sejam fornecidas da linha de comando, de um arquivo de dados, de um arquivo de configuração ou do arquivo IDL.

Seu aplicativo cliente também pode consultar um banco de dados de serviço de nome para obter informações de ponto de extremidade conhecidas.

## <a name="using-dynamic-endpoints"></a>Usando pontos de extremidade dinâmicos

O número de pontos de extremidade para um servidor específico e uma sequência de protocolo específica geralmente são limitados. Por exemplo, quando você usa a sequência de protocolo [ncacn \_ ip \_ tcp,](/windows/desktop/Midl/ncacn-ip-tcp) indicando que a comunicação de rede RPC ocorre usando TCP/IP, apenas um número limitado de portas está disponível (a maioria dos sistemas tem apenas o intervalo de 1025 a 5000 abertos). As bibliotecas de tempo de executar RPC permitem atribuir pontos de extremidade dinamicamente, conforme necessário. Como o número de UUIDs de interface possíveis é praticamente ilimitado, o uso da interface UUID para direcionar a chamada oferece mais espaço para expansão e mais flexibilidade.

Por padrão, as funções de biblioteca em tempo de executar RPC pesquisam informações de ponto de extremidade quando consultam um banco de dados de serviço de nome. Se o ponto de extremidade for dinâmico, o nome do banco de dados de serviço não conterá informações de ponto de extremidade. No entanto, a consulta dará ao programa cliente o nome de um servidor. Em seguida, ele pode pesquisar o mapa de ponto de extremidade do servidor.

Se o cliente precisar fazer uma chamada de procedimento remoto usando um ponto de extremidade dinâmico, o método preferencial será fazer a chamada em um handle de associação parcialmente vinculado. O tempo de executar RPC resolve o ponto de extremidade de forma transparente. Esse método é superior ao uso da [**função RpcEpResolveBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) pois permite mecanismos avançados de cache no tempo de executar RPC.

Se for necessário um controle mais específico sobre a seleção de ponto de extremidade, os clientes poderão pesquisar no mapa de ponto de extremidade uma entrada por vez chamando as funções [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin), [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)e [**RpcMgmtEpEltInqDone.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportando pontos de extremidade conhecidos para o banco de dados de mapa de ponto de extremidade

É possível combinar as duas abordagens para localizar pontos de extremidade, especialmente quando um sistema distribuído faz a transição de um modelo de ponto de extremidade conhecido para um modelo de ponto de extremidade dinâmico. Em tais transições, uma versão intermediária do servidor usará um ponto de extremidade conhecido, mas também registrará o ponto de extremidade conhecido com o banco de dados de mapa do ponto de extremidade. Essa abordagem permite que clientes que usam um ponto de extremidade conhecido e clientes que usam um ponto de extremidade dinâmico se conectem. Depois que todos os servidores são atualizados, uma nova versão do cliente pode ser implantada que usa apenas pontos de extremidade dinâmicos. Depois que todos os clientes são atualizados, uma versão final do servidor pode parar de usar pontos de extremidade conhecidos e começar a usar apenas pontos de extremidade dinâmicos.

Essa abordagem permite um caminho de transição para aplicativos que iniciaram com um ponto de extremidade conhecido, mas que querem migrar para um ponto de extremidade dinâmico sem exigir uma atualização simultânea de todos os servidores e clientes.

 

 