---
description: Os clientes e os servidores devem obter credenciais antes de poderem estabelecer um contexto de segurança para a troca de mensagens.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Obtendo credenciais de resumo padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d5a0bb39f59680f2b5232dae1e6cc5c83673cf31c7cc3e0aa1325d5641e161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786584"
---
# <a name="obtaining-default-digest-credentials"></a>Obtendo credenciais de resumo padrão

Os clientes e os servidores devem obter [*credenciais*](../secgloss/c-gly.md) antes de poderem estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) para a troca de mensagens. O comportamento padrão da função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) é fornecer credenciais para a entidade de segurança associada à [*sessão*](../secgloss/s-gly.md)de logon atual.

O exemplo a seguir demonstra uma chamada do lado do servidor para obter as credenciais padrão.


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



A chamada do lado do cliente para credenciais padrão é idêntica, exceto que o terceiro parâmetro deve especificar SECPKG de saída de credenciais \_ \_ para indicar que o cliente usará o identificador de credenciais retornado pela função.

Para obter um exemplo que demonstra a obtenção de credenciais para uma entidade de segurança que não seja o usuário conectado, consulte [obtendo credenciais alternativas](obtaining-alternate-digest-credentials.md).

 

 
