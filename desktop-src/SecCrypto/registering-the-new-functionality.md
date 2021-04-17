---
description: O suporte para registrar a nova funcionalidade em um registro do sistema deve ser fornecido na nova DLL junto com a nova função.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Registrando a nova funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779944"
---
# <a name="registering-the-new-functionality"></a>Registrando a nova funcionalidade

O suporte para registrar a nova funcionalidade em um registro do sistema deve ser fornecido na nova DLL junto com a nova função. As [funções de suporte a OID](cryptography-functions.md) fornecem assistência com esse registro. Regsvr32.exe registra novas funções. Essa ferramenta está incluída no Windows.

A nova DLL deve fornecer pontos de entrada [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para uso pelo Regsvr32.exe. As funções de [*CryptoAPI*](../secgloss/c-gly.md) , como [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) ou [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), podem ser usadas nesses pontos de entrada, conforme mostrado no exemplo a seguir.


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



Este exemplo deve ser compilado e vinculado à nova DLL. Esses dois pontos de entrada, juntamente com o ponto de entrada da função, devem ser exportados.

Para instalar a nova funcionalidade em um computador, execute Regsvr32.exe em um prompt de comando, especificando o nome e o caminho da nova DLL. Regsvr32.exe acessa a função [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) por meio do ponto de entrada da função [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) e registra a nova função e a dll.

 

 
