---
title: Erro comum supondo que RpcServerRegisterAuthInfo impede que usuários não autorizados chamem seu servidor
description: Quando os provedores de segurança são registrados no servidor com a função RpcServerRegisterAuthInfo, uma opção é adicionada, não um requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636848"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Erro comum: supondo que RpcServerRegisterAuthInfo impede que usuários não autorizados chamem seu servidor

Quando os provedores de segurança são registrados no servidor com a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , uma opção é adicionada, não um requisito. Isso significa que os registros anteriores com **RpcServerRegisterAuthInfo** não são substituídos. Isso também significa que clientes não autenticados ainda podem se conectar. Chamando a função **RpcServerRegisterAuthInfo** , os clientes não autenticados não são permitidos da conexão; Eles ainda podem se conectar, mas chamadas de função, como [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , falharão. Assim, quando a função **RpcServerRegisterAuthInfo** é chamada, os invasores potenciais não foram desfeitos — em vez disso, os clientes que precisam ter acesso têm a oportunidade de provar sua identidade. As verificações ainda devem estar em vigor para determinar se os invasores potenciais estão tentando se conectar.

 

 




