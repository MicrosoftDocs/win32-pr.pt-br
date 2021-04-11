---
description: Os clientes e os servidores devem obter credenciais antes de poderem estabelecer um contexto de segurança para a troca de mensagens.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Obtendo credenciais de resumo padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169373"
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

 

 
