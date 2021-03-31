---
title: Qual provedor de segurança usar
description: Todas as outras coisas são iguais, use RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635925"
---
# <a name="which-security-provider-to-use"></a>Qual provedor de segurança usar

Todas as outras coisas são iguais, use RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate. Cada um fornece o serviço mais escalonável e seguro. Se você usar RPC \_ C \_ Authn \_ GSS \_ Negotiate no servidor, isso permitirá que clientes de nível inferior, como clientes NTLM, se conectem ao seu servidor. Se isso for indesejável, limite a escolha somente para RPC \_ C \_ Authn \_ GSS \_ Kerberos ou chame [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para determinar qual provedor de segurança o cliente está usando e negar acesso a clientes usando NTLM. O método preferencial para estabelecer qual provedor de segurança o cliente está usando é a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




