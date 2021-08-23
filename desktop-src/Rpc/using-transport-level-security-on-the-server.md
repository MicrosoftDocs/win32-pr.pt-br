---
title: Usando a segurança em nível de transporte no servidor
description: Usando a segurança em nível de transporte no servidor com RPC (chamada de procedimento remoto).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando segurança em nível de transporte no servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abd1f072f249336f4804aed56fb1122556596c43286383b763839d988a2406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010584"
---
# <a name="using-transport-level-security-on-the-server"></a>Usando a segurança em nível de transporte no servidor

Esta seção apresenta discussões sobre a segurança em nível de transporte, dividida nos seguintes tópicos:

-   [Usando Transport-Level segurança no cliente](using-transport-level-security-on-the-client.md)

Quando você usa [ncacn \_ NP](/windows/desktop/Midl/ncacn-np) ou [Ncalrpc](/windows/desktop/Midl/ncalrpc) como a sequência de protocolo, o servidor especifica um descritor de segurança para o ponto de extremidade no momento em que seleciona a sequência de protocolo. Para obter mais informações sobre sequências de protocolo, consulte [especificando sequências de protocolo](specifying-protocol-sequences.md). Seu aplicativo fornece o descritor de segurança como um parâmetro adicional (uma extensão para os parâmetros padrão do uso-DCE) em todas as funções que começam com os prefixos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). O descritor de segurança controla se um cliente pode se conectar ao ponto de extremidade.

Cada processo e thread é associado a um token de segurança. Esse token inclui um descritor de segurança padrão que é usado para todos os objetos que o processo cria, como o ponto de extremidade. Se o seu aplicativo não especificar um descritor de segurança ao chamar uma função com os prefixos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), a biblioteca de tempo de execução do RPC aplicará o descritor de segurança padrão do token de segurança do processo ao ponto de extremidade.

Para garantir que o aplicativo de servidor seja acessível a todos os clientes, o administrador deve iniciar o aplicativo de servidor em um processo que tenha um descritor de segurança padrão que todos os clientes possam usar. Em geral, somente os processos do sistema têm um descritor de segurança padrão.

Para obter mais informações sobre essas funções e as funções [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 