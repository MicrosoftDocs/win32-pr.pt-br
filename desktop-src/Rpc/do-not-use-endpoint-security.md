---
title: Não usar a segurança do ponto de extremidade
description: O Endpoint Security é um modelo de segurança no qual um descritor de segurança é fornecido quando um ponto de extremidade é criado com o grupo RpcServerUseProtseq \ de funções RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635722"
---
# <a name="do-not-use-endpoint-security"></a>Não usar a segurança do ponto de extremidade

O Endpoint Security é um modelo de segurança no qual um descritor de segurança é fornecido quando um ponto de extremidade é criado com o grupo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* de funções RPC. Não use esse modelo de segurança. Não forneça descritores de segurança para essas funções. Na melhor das hipóteses, esse método é um desperdício de recursos de CPU. Na pior das hipóteses, em muitos ambientes, é possível burlar o descritor de segurança, pois deve [ser cauteloso com outros pontos de extremidade RPC em execução na mesma](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) seção de processo exemplifica.

A segurança do ponto de extremidade existe somente para compatibilidade com versões anteriores.

 

 




