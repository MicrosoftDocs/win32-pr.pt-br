---
title: Escolhendo as opções de QOS de segurança
description: As opções de QOS de segurança são passadas como parte do parâmetro SecurityQOS fornecido para a função RpcBindingSetAuthInfoEx. Use as práticas recomendadas a seguir.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c943fd9e2b4104de87a24c6078499fa38acdf1b6d1ea2122bf9d3063cd80f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932192"
---
# <a name="choosing-security-qos-options"></a>Escolhendo as opções de QOS de segurança

As opções de QOS de segurança são passadas como parte do parâmetro *SecurityQOS* fornecido para a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Use as práticas recomendadas a seguir.

## <a name="use-mutual-authentication"></a>Usar autenticação mútua

A autenticação mútua verdadeira está disponível apenas para determinados provedores de segurança: Negotiate (ao negociar Kerberos), Kerberos e Schannel. O NTLM não oferece suporte à autenticação mútua. O uso da autenticação mútua exige que um nome de entidade de servidor bem formado seja fornecido. Muitos desenvolvedores usam a seguinte prática de segurança com falha: o servidor é chamado para solicitar seu nome principal ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) e, em seguida, ele solicita indistintamente a autenticação mútua usando esse nome de entidade. Essa abordagem quebra toda a ideia de autenticação mútua; a ideia de autenticação mútua é que apenas determinados servidores são chamados porque são confiáveis para analisar e lidar com seus dados. Usando a prática de segurança com falhas que você acabou de descrever, os desenvolvedores fornecem seus dados a qualquer pessoa inteligente o suficiente para retornar seu nome.

Por exemplo, se o software cliente deve chamar apenas um servidor em execução nas contas de Joe, Pete ou Alice, a função [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) deve ser chamada e o nome enviado deve ser verificado. Se for Joe, Pete ou Alice, a autenticação mútua deverá ser solicitada usando o nome principal do servidor. Isso garante que ambas as metades da conversa vão para a mesma entidade de segurança.

Se o software cliente deve chamar um serviço em execução apenas na conta de Joe, redija diretamente o nome principal do servidor de Joe e faça a chamada. Se o servidor não for Joe, a chamada simplesmente falhará.

muitas vezes, os serviços são executados como Windows serviços do sistema, o que significa que eles são executados na conta do computador. A autenticação mútua e a criação de um nome principal de servidor ainda são recomendadas.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Use o Impersonationtype mais baixo que permite que a chamada passe por

Essa prática recomendada é bastante auto-explicativa. Mesmo que a autenticação mútua seja usada, não conceda ao servidor mais direitos do que o necessário; um servidor legítimo pode ter sido comprometido e, embora os dados enviados entrem em mãos erradas nesses casos, pelo menos o servidor não será capaz de acessar outros dados na rede em seu nome. Alguns servidores rejeitarão uma chamada que não tem informações suficientes para determinar e possivelmente representar o chamador. Além disso, lembre-se de que algumas sequências de protocolo dão suporte à segurança de nível de transporte ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**Ncalrpc**](/windows/desktop/Midl/ncalrpc)). Nesses casos, o servidor sempre poderá representá-lo se você especificar um nível de representação suficientemente alto por meio do parâmetro *networkoptions* ao criar o identificador de associação.

Por fim, alguns provedores de segurança ou transportes podem aumentar de forma transparente um nível mais alto do que o especificado. Ao desenvolver um programa, certifique-se de tentar fazer chamadas com o Impersonationtype pretendido e verificar se você está obtendo um Impersonationtype maior no servidor.

 

 