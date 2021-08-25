---
description: O exemplo a seguir mostra as etapas para obter uma estrutura CERT CONTEXT que contém um certificado; você deve selecionar um certificado e um armazenamento de certificados apropriados \_ para seu aplicativo.
ms.assetid: 31d7a8bd-729f-4db7-8e22-25d14296c0c4
title: Obter um certificado para schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b648f55cdfe68bc6c6b1b02b9c0d5bc715fe4efeaad70d25072b4709a2cd0114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883136"
---
# <a name="getting-a-certificate-for-schannel"></a>Obter um certificado para schannel

O exemplo a seguir mostra as etapas para obter uma estrutura [**CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) que contém um certificado; você deve selecionar um certificado e um armazenamento de certificados apropriados para seu aplicativo.

Este exemplo demonstra [*como*](/windows/desktop/SecGloss/c-gly) abrir um armazenamento de certificados e localizar um certificado que será passado para a função [**AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) por meio da estrutura [**\_ CRED SCHANNEL.**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred)


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



 

 
