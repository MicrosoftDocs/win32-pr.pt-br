---
title: Escolhendo as opções de QOS de segurança
description: As opções de QOS de segurança são passadas como parte do parâmetro SecurityQOS fornecido para a função RpcBindingSetAuthInfoEx. Use as práticas recomendadas a seguir.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759346"
---
# <a name="choosing-security-qos-options"></a>Escolhendo as opções de QOS de segurança

As opções de QOS de segurança são passadas como parte do parâmetro *SecurityQOS* fornecido para a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Use as práticas recomendadas a seguir.

## <a name="use-mutual-authentication"></a>Usar autenticação mútua

A autenticação mútua verdadeira está disponível apenas para determinados provedores de segurança: Negotiate (ao negociar Kerberos), Kerberos e Schannel. O NTLM não oferece suporte à autenticação mútua. O uso da autenticação mútua exige que um nome de entidade de servidor bem formado seja fornecido. Muitos desenvolvedores usam a seguinte prática de segurança com falha: o servidor é chamado para solicitar seu nome principal ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) e, em seguida, ele solicita indistintamente a autenticação mútua usando esse nome de entidade. Essa abordagem quebra toda a ideia de autenticação mútua; a ideia de autenticação mútua é que apenas determinados servidores são chamados porque são confiáveis para analisar e lidar com seus dados. Usando a prática de segurança com falhas que você acabou de descrever, os desenvolvedores fornecem seus dados a qualquer pessoa inteligente o suficiente para retornar seu nome.

Por exemplo, se o software cliente deve chamar apenas um servidor em execução nas contas de Joe, Pete ou Alice, a função [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) deve ser chamada e o nome enviado deve ser verificado. Se for Joe, Pete ou Alice, a autenticação mútua deverá ser solicitada usando o nome principal do servidor. Isso garante que ambas as metades da conversa vão para a mesma entidade de segurança.

Se o software cliente deve chamar um serviço em execução apenas na conta de Joe, redija diretamente o nome principal do servidor de Joe e faça a chamada. Se o servidor não for Joe, a chamada simplesmente falhará.

Muitas vezes, os serviços são executados como serviços de sistema do Windows, o que significa que eles são executados na conta do computador. A autenticação mútua e a criação de um nome principal de servidor ainda são recomendadas.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Use o Impersonationtype mais baixo que permite que a chamada passe por

Essa prática recomendada é bastante auto-explicativa. Mesmo que a autenticação mútua seja usada, não conceda ao servidor mais direitos do que o necessário; um servidor legítimo pode ter sido comprometido e, embora os dados enviados entrem em mãos erradas nesses casos, pelo menos o servidor não será capaz de acessar outros dados na rede em seu nome. Alguns servidores rejeitarão uma chamada que não tem informações suficientes para determinar e possivelmente representar o chamador. Além disso, lembre-se de que algumas sequências de protocolo dão suporte à segurança de nível de transporte ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**Ncalrpc**](/windows/desktop/Midl/ncalrpc)). Nesses casos, o servidor sempre poderá representá-lo se você especificar um nível de representação suficientemente alto por meio do parâmetro *networkoptions* ao criar o identificador de associação.

Por fim, alguns provedores de segurança ou transportes podem aumentar de forma transparente um nível mais alto do que o especificado. Ao desenvolver um programa, certifique-se de tentar fazer chamadas com o Impersonationtype pretendido e verificar se você está obtendo um Impersonationtype maior no servidor.

 

 