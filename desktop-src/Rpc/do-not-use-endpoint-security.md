---
title: Não usar a segurança do ponto de extremidade
description: A segurança do ponto de extremidade é um modelo de segurança no qual um descritor de segurança é dado quando um ponto de extremidade é criado com o grupo de funções RPC RpcServerUseProtseq\.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d302ec0d331eaadb3291e36b30084264b4a6331745110fc642dd2ede02c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930693"
---
# <a name="do-not-use-endpoint-security"></a>Não usar a segurança do ponto de extremidade

A segurança do ponto de extremidade é um modelo de segurança no qual um descritor de segurança é dado quando um ponto de extremidade é criado com o grupo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) de \* funções RPC. Não use esse modelo de segurança. Não dê descritores de segurança a essas funções. Na melhor das formas, esse método é um desperdício de recursos de CPU. Na pior das hipóteses, em muitos ambientes, é possível contornar o descritor de segurança, pois a seção Be [Wary of Other RPC Endpoints](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) Running In the Same Process exemplifica.

A segurança do ponto de extremidade existe apenas para compatibilidade com compatibilidade com backward.

 

 




