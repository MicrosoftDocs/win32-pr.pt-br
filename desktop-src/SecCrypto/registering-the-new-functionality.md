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
# <a name="registering-the-new-functionality"></a><span data-ttu-id="91caa-103">Registrando a nova funcionalidade</span><span class="sxs-lookup"><span data-stu-id="91caa-103">Registering the New Functionality</span></span>

<span data-ttu-id="91caa-104">O suporte para registrar a nova funcionalidade em um registro do sistema deve ser fornecido na nova DLL junto com a nova função.</span><span class="sxs-lookup"><span data-stu-id="91caa-104">Support for registering the new functionality in a system registry must be provided in the new DLL along with the new function.</span></span> <span data-ttu-id="91caa-105">As [funções de suporte a OID](cryptography-functions.md) fornecem assistência com esse registro.</span><span class="sxs-lookup"><span data-stu-id="91caa-105">[OID Support Functions](cryptography-functions.md) provide assistance with this registration.</span></span> <span data-ttu-id="91caa-106">Regsvr32.exe registra novas funções.</span><span class="sxs-lookup"><span data-stu-id="91caa-106">Regsvr32.exe registers new functions.</span></span> <span data-ttu-id="91caa-107">Essa ferramenta está incluída no Windows.</span><span class="sxs-lookup"><span data-stu-id="91caa-107">This tool is included with Windows.</span></span>

<span data-ttu-id="91caa-108">A nova DLL deve fornecer pontos de entrada [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para uso pelo Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="91caa-108">The new DLL must provide [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entry points for use by Regsvr32.exe.</span></span> <span data-ttu-id="91caa-109">As funções de [*CryptoAPI*](../secgloss/c-gly.md) , como [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) ou [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), podem ser usadas nesses pontos de entrada, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="91caa-109">[*CryptoAPI*](../secgloss/c-gly.md) functions, such as [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) or [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), can be used within these entry points, as shown in the following example.</span></span>


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



<span data-ttu-id="91caa-110">Este exemplo deve ser compilado e vinculado à nova DLL.</span><span class="sxs-lookup"><span data-stu-id="91caa-110">This example must be compiled and linked into the new DLL.</span></span> <span data-ttu-id="91caa-111">Esses dois pontos de entrada, juntamente com o ponto de entrada da função, devem ser exportados.</span><span class="sxs-lookup"><span data-stu-id="91caa-111">These two entry points, along with the function entry point, must be exported.</span></span>

<span data-ttu-id="91caa-112">Para instalar a nova funcionalidade em um computador, execute Regsvr32.exe em um prompt de comando, especificando o nome e o caminho da nova DLL.</span><span class="sxs-lookup"><span data-stu-id="91caa-112">To install the new functionality on a computer, run Regsvr32.exe from a command prompt, specifying the name and path of the new DLL.</span></span> <span data-ttu-id="91caa-113">Regsvr32.exe acessa a função [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) por meio do ponto de entrada da função [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) e registra a nova função e a dll.</span><span class="sxs-lookup"><span data-stu-id="91caa-113">Regsvr32.exe accesses the [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) function through the [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) function entry point and registers the new function and DLL.</span></span>

 

 
