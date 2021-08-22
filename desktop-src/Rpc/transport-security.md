---
title: Segurança de transporte
description: Embora esse não seja o método preferencial, você pode usar as configurações de segurança que o transporte de pipe nomeado oferece para adicionar recursos de segurança ao seu aplicativo distribuído.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d92a0c9f0b31392d265c1c60bd201d088af8e8ff0b10ac4e09e274da92d2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011204"
---
# <a name="transport-security"></a>Segurança de transporte

Embora esse não seja o método preferencial, você pode usar as configurações de segurança que o transporte de pipe nomeado oferece para adicionar recursos de segurança ao seu aplicativo distribuído. Essas configurações de segurança são usadas com as funções RPC da Microsoft que começam com os prefixos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)e as funções [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Se você estiver executando um aplicativo que é um serviço e estiver usando o NTLM para segurança, deverá adicionar uma dependência de serviço explícita para seu aplicativo. O Secur32.dll chamará o SCM (Service Control Manager) para iniciar o serviço de pacote de segurança NTLM. No entanto, um aplicativo RPC que é um serviço e está em execução como um sistema, também deve entrar em contato com a SC, a menos que ele esteja se conectando a outro serviço no mesmo computador.

 

 

 




