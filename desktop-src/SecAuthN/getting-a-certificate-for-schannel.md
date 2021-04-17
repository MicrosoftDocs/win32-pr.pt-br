---
description: O exemplo a seguir mostra as etapas para obter uma \_ estrutura de contexto de certificado que contém um certificado; você deve selecionar um certificado e um repositório de certificados apropriados para seu aplicativo.
ms.assetid: 31d7a8bd-729f-4db7-8e22-25d14296c0c4
title: Obtendo um certificado para Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf7f311ac31fe2ff033d4b57f7d04bd1f42424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752829"
---
# <a name="getting-a-certificate-for-schannel"></a><span data-ttu-id="b60f6-103">Obtendo um certificado para Schannel</span><span class="sxs-lookup"><span data-stu-id="b60f6-103">Getting a Certificate for Schannel</span></span>

<span data-ttu-id="b60f6-104">O exemplo a seguir mostra as etapas para obter uma estrutura de [**\_ contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado que contém um certificado; você deve selecionar um certificado e um repositório de certificados apropriados para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b60f6-104">The following example shows the steps to obtain a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure that contains a certificate; you should select a certificate and certificate store that are appropriate for your application.</span></span>

<span data-ttu-id="b60f6-105">Este exemplo demonstra como abrir um [*repositório de certificados*](/windows/desktop/SecGloss/c-gly) e localizar um certificado que será passado para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , por meio da estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) .</span><span class="sxs-lookup"><span data-stu-id="b60f6-105">This example demonstrates opening a [*certificate store*](/windows/desktop/SecGloss/c-gly) and locating a certificate that will be passed to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, by means of the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "crypt32.lib")

#define MACHINE_NAME "example server"

PCCERT_CONTEXT getServerCertificate ()
{
  HCERTSTORE hMyCertStore = NULL;
  PCCERT_CONTEXT aCertContext = NULL;
  
  //-------------------------------------------------------
  // Open the My store, also called the personal store.
  // This call to CertOpenStore opens the Local_Machine My 
  // store as opposed to the Current_User's My store.

    hMyCertStore = CertOpenStore(CERT_STORE_PROV_SYSTEM,
                                 X509_ASN_ENCODING,
                                 0,
                                 CERT_SYSTEM_STORE_LOCAL_MACHINE,
                                 L"MY");

  if (hMyCertStore == NULL) 
  {
    printf("Error opening MY store for server.\n");
    goto cleanup;
  }
  //-------------------------------------------------------
  // Search for a certificate with some specified
  // string in it. This example attempts to find
  // a certificate with the string "example server" in
  // its subject string. Substitute an appropriate string
  // to find a certificate for a specific user.

  aCertContext = CertFindCertificateInStore(hMyCertStore, 
                  X509_ASN_ENCODING, 
                  0,
                  CERT_FIND_SUBJECT_STR_A,
                  MACHINE_NAME, // use appropriate subject name
                  NULL
  );
  
  if (aCertContext == NULL)
  {
    printf("Error retrieving server certificate.");
    goto cleanup;
  }
cleanup:
  if(hMyCertStore)
  {
      CertCloseStore(hMyCertStore,0);
  }
  return aCertContext;
}
```



 

 
