---
description: O exemplo a seguir demonstra como um cliente típico obterá credenciais Schannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Obtendo credenciais Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296832"
---
# <a name="getting-schannel-credentials"></a>Obtendo credenciais Schannel

O exemplo a seguir demonstra como um cliente típico obterá credenciais Schannel. O exemplo segue a prática recomendada de usar os padrões do sistema para codificações e níveis de codificação. Isso permite que o pacote Schannel use os algoritmos mais fortes possíveis para proteger o canal.


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



A principal diferença entre a solicitação do lado do cliente e do servidor para credenciais é que o servidor deve fornecer um certificado usando uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) da seguinte maneira:


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



A função de exemplo *getServerCertificate* é uma função de espaço reservado para essa atividade específica do aplicativo. Para obter um exemplo de implementação da função *getServerCertificate* , consulte [obtendo um certificado](getting-a-certificate-for-schannel.md).

> [!Note]  
> Ao solicitar as credenciais a serem usadas pelo servidor, altere o terceiro parâmetro (*fCredentialUse*) da função [**falha ACQUIRECREDENTIALSHANDLE**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) de saída SECPKG de \_ credenciais \_ para SECPKG de entrada de credenciais \_ \_ .

 

 

 
