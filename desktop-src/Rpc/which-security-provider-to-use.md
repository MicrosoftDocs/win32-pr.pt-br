---
title: Qual provedor de segurança usar
description: Todas as outras coisas são iguais, use RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010444"
---
# <a name="which-security-provider-to-use"></a>Qual provedor de segurança usar

Todas as outras coisas são iguais, use RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate. Cada um fornece o serviço mais escalonável e seguro. Se você usar RPC \_ C \_ Authn \_ GSS \_ Negotiate no servidor, isso permitirá que clientes de nível inferior, como clientes NTLM, se conectem ao seu servidor. Se isso for indesejável, limite a escolha somente para RPC \_ C \_ Authn \_ GSS \_ Kerberos ou chame [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para determinar qual provedor de segurança o cliente está usando e negar acesso a clientes usando NTLM. O método preferencial para estabelecer qual provedor de segurança o cliente está usando é a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




